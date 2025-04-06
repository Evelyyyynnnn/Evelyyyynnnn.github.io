---
tags: Interview
date: 2025-04-11 10:15:38
---

Here I will record some ordinary SQL questions for exercise and my way to exercise SQL is always to *learn from the real questions*

```sql
-- 创建图文点赞数据表
CREATE TABLE `table` (
    `p_date` DATE NOT NULL,          -- 时间分区
    `content_id` INT NOT NULL,       -- 图文内容ID
    `like_cnt` INT DEFAULT 0,        -- 图文当天累计点赞数
    PRIMARY KEY (`p_date`, `content_id`)
) CHARSET=utf8;

-- 插入示例数据
INSERT INTO `table` VALUES
('2025-09-01', 1, 100),
('2025-09-02', 1, 150),
('2025-09-03', 1, 200),
('2025-09-01', 2, 50),
('2025-09-02', 2, 80),
('2025-09-03', 2, 120),
('2025-09-01', 3, 300),
('2025-09-02', 3, 400),
('2025-09-03', 3, 500);

-- 查询9.1-9.30每天的点赞增量
SELECT 
    t1.p_date,
    t1.content_id,
    t1.like_cnt AS like_cnt,
    COALESCE(t2.like_cnt, 0) AS like_cnt_1day,
    (t1.like_cnt - COALESCE(t2.like_cnt, 0)) AS like_cnt_diff
FROM `table` t1
LEFT JOIN `table` t2
ON t1.content_id = t2.content_id AND t1.p_date = DATE_ADD(t2.p_date, INTERVAL 1 DAY)
WHERE t1.p_date BETWEEN '2025-09-01' AND '2025-09-30'
ORDER BY like_cnt_diff DESC
LIMIT 100;
```


| p_date      | content_id | like_cnt | like_cnt_1day | like_cnt_diff |
|-------------|------------|----------|---------------|---------------|
| 2025-09-01  | 3          | 300      | 0             | 300           |
| 2025-09-01  | 1          | 100      | 0             | 100           |
| 2025-09-02  | 3          | 400      | 300           | 100           |
| 2025-09-03  | 3          | 500      | 400           | 100           |
