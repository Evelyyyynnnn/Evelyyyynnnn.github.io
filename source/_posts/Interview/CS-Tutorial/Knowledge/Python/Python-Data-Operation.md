---
tags: Interview
date: 2025-04-11 10:15:38
---



```Python
data['DateTime'] = pd.to_datetime(data['DateTime'])
#use copy to avoid the influence to old databasemen
filtered_data = data[data['DateTime'] > '2020-12-31'].copy()  
filtered_data = data[data['DateTime'] > '2020-12-31'].copy(deep=True)
#准确来说只有deep copy之下原数据才不受到影响
filtered_data.head()


filtered_data.loc[:, 'Raw Close (PRCCD)'] = pd.to_numeric(filtered_data['Raw Close (PRCCD)'], errors='coerce')
filtered_data = filtered_data.dropna(subset=['Raw Close (PRCCD)'])

# use.loc to avoid the SettingWithCopyWarning problem
filtered_data.loc[:, 'Daily Return'] = filtered_data['Raw Close (PRCCD)'].pct_change()
# 避免链式赋值：直接使用 filtered_data['High Watermark'] = ... 可能会导致链式赋值问题，而 .loc 可以避免这种情况

avg_daily_return = filtered_data['Daily Return'].mean()

annualized_return = avg_daily_return * 251
print(f"Average Annualized Return: {annualized_return:.4f}")

```