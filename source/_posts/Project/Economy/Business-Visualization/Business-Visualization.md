---
title: Economy & Business- Visulization
tags: Project 
date: 2023-09-11 10:15:38
---
*<small>[Home](/About/index.html) > [Project](/tags/Project/index.html) > [Economy&Business](/2023/09/11/Project/Economy/Economy/index.html) > **[Business Visualization](/2023/09/11/Project/Economy/Business-Visualization/Business-Visualization/index.html)</small>***
<style>
.image-container {
        display: flex;
        justify-content: space-between; /* 让图片均匀分布在一行中 */
        position: relative;
        hover ~ img {
        filter: blur(100000px); /* 鼠标碰到按钮后，图片变模糊 */
        }
    }
</style>

<h3 id="power-bi-section">1. Power BI</h3>

[Power BI](https://www.microsoft.com/en-us/power-platform/products/power-bi/) offers a wide range of applications in the business world.Here I analyzed the performance of various groups within a gym over the past two years, including different regions, stores, and types of coaches, conducting a correlational analysis.
> Project Address: [here](/zip/Business-Visualization-Case.pbix)


<div style="display: flex; justify-content: center;">
    <img src="https://s2.loli.net/2024/01/05/Vu9eGUZYsjSXn1E.png" style="width: 50%; height: auto; margin-right: 10px;">
    <img src="https://s2.loli.net/2024/01/05/igIpwYW7R9EXqHO.png" style="width: 50%; height: auto;">
</div>

### 2. [Thinkcell](https://www.think-cell.com/en) and [Tableau](https://www.tableau.com/en-gb)

<h4 id="tableau-section">2.1 Goldman Sachs Stock Pitch:</h4> 
Here we select Bilibili as the target company within an industry and forecast its revenue and other metrics by analyzing the macro environment post-pandemic recovery and the rising trend of Bilibili's game business.

> Bilibili Valuation:[project address](/pdf/Group6_BILI_Stock_Pitch.pdf)

<div style="display: flex; justify-content: center;">
    <img src="https://s2.loli.net/2024/01/05/cYTeUGmha5yONR7.png" style="width: 50%; height: auto; margin-right: 10px;">
    <img src="https://s2.loli.net/2024/01/05/grAUdcLNnChQkJf.png" style="width: 50%; height: auto;">
</div>

#### 2.2 SHARE Case Competition:
This case offers us more opportunities to analyze the nascent new energy industry and the synergistic effects with upstream parts manufacturers, downstream B2C and B2B consumers, plus internet companies.
> Sustainable Vehicle Macro Overview:[project address](/zip/ShARE-Sustainable-vehicle-development.pdf)

<div style="display: flex; justify-content: center;">
    <img src="https://s2.loli.net/2024/01/05/Xc9m7HNvzpPZ4h2.png" style="width: 50%; height: auto; margin-right: 10px;">
    <img src="https://s2.loli.net/2024/01/05/oxBV7ZkjNPuDzG3.png" style="width: 50%; height: auto;">
</div>
 
<h4 id="thinkcell-section">2.3 Roland Berger Consulting Challenge:</h4> 
I analyzed the infrastructure industry for this case, offering constructive suggestions for airports' unseen strategies, such as expansion or outsourcing, based on linear metrics like passenger flow.

> Airport Mode Analysis:[project address](/zip/Airport-Planning-Roland-Berger-Challenge.pdf)

<div style="display: flex; justify-content: center;">
    <img src="https://s2.loli.net/2024/01/05/QPy4bhzenGOaVsE.png" style="width: 50%; height: auto; margin-right: 10px;">
    <img src="https://s2.loli.net/2024/01/05/Ng1PesoS7zwmFBD.png" style="width: 50%; height: auto;">
</div>

#### 2.4 Food Ingedient Industry:
I focused particularly on the disruptive impact of technologies like genetic engineering on traditional sectors. It explores industry development patterns and ROI through data mining, data cleansing, and regression analysis.
> MA Report:[project address](/zip/Food-Ingredient-MA-targeted-Report.pdf)

<div style="display: flex; justify-content: center;">
    <img src="https://s2.loli.net/2024/01/05/ohsc5bfn3BQCySX.png" style="width: 50%; height: auto; margin-right: 10px;">
    <img src="https://s2.loli.net/2024/01/05/w9lSQCxdGRfvhN4.png" style="width: 50%; height: auto;">
</div>

### 3. Python
Here I used applied R on cluster to do the customer profile engineering job and make suggestions to the medicine sales
<div style="display: flex; justify-content: center; align-items: center;">
    <img src="https://s2.loli.net/2024/01/07/hTAWm43S7daYowL.jpg" style="max-width: 50%; height: auto;">
</div>

> Project [Code](https://drive.google.com/file/d/113H0X4zxGXa93fTv2rb60Ar2lkD9SN-s/view?usp=sharing)

### 4. Neo4j
Here is the representation of the [Knowledge Map](/2023/09/11/Project/Economy/Business-Visualization/Knowledge-Map/index.html)

### 5.[Website](https://www.founderjar.com/best-data-visualization-tools/)
You could refer to my [tutorial](/2023/09/11/Interview/CS-Tutorial/index.html) where I included 3 different ways to do about website visualization in python 



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Network Graph</title>
    <style>
        .link {
            stroke-width: 2px;
            /* stroke-dasharray: 5, 5; removed dashed line style */
        }
        .link.management { stroke: #7DC69B; }
        .node text {
            pointer-events: none;
            font: 12px sans-serif;
        }
        svg {
            display: block;
            margin: auto; /* Center the SVG */
            border: 1px solid #ccc; /* Optional: Add a border for debugging */
        }
    </style>
</head>
<body>
    <script src="https://d3js.org/d3.v6.min.js"></script>
    <script>
        // Set the dimensions of the SVG canvas
        const width = 1200; // Increased width
        const height = 850; // Increased height
        const data = [
     {
          "subject": "Pan Gang",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Legal Representative, Beneficial Owner, Chairman, Executive Director, President"
     },
     {
          "subject": "Zhao Chengxia",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Executive Director, President, Chief Financial Officer"
     },
     {
          "subject": "Wang Xiaogang",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Executive Director, President"
     },
     {
          "subject": "Lu Gang",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Director"
     },
     {
          "subject": "Chaolu",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Director"
     },
     {
          "subject": "Wang Yanfang",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Employee Director"
     },
     {
          "subject": "Zhao Ying",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Employee Director"
     },
     {
          "subject": "Cai Yuanming",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Independent Director"
     },
     {
          "subject": "Shi Fang",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Independent Director"
     },
     {
          "subject": "Ji Shao",
          "relation": "management",
          "object": "Inner Mongolia Yili Industrial Group Co., Ltd.",
          "identity": "Independent Director"
     },
     {
          "subject": "Chen Lang",
          "relation": "management",
          "object": "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.",
          "identity": "Beneficial Owner, Chairman"
     },
     {
          "subject": "Lu Minfang",
          "relation": "management",
          "object": "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.",
          "identity": "Legal Representative, General Manager, Director"
     },
     {
          "subject": "Zhang Ping",
          "relation": "management",
          "object": "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.",
          "identity": "Director"
     },
     {
          "subject": "Wen Yongping",
          "relation": "management",
          "object": "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.",
          "identity": "Director"
     },
     {
          "subject": "Wang Yan",
          "relation": "management",
          "object": "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.",
          "identity": "Director"
     },
     {
          "subject": "Guo Lidong",
          "relation": "management",
          "object": "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.",
          "identity": "Chairman of the Supervisory Board"
     },
     {
          "subject": "Liu Enduo",
          "relation": "management",
          "object": "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.",
          "identity": "Supervisor"
     },
     {
          "subject": "Li Xiuli",
          "relation": "management",
          "object": "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.",
          "identity": "Supervisor"
     },
     {
          "subject": "Huang Liming",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Legal Representative, Beneficial Owner"
     },
     {
          "subject": "Ben Min",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Director, General Manager"
     },
     {
          "subject": "Lu Qikai",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Director"
     },
     {
          "subject": "Xu Meihua",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Employee Director"
     },
     {
          "subject": "Mao Huigang",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Independent Director"
     },
     {
          "subject": "Gao Li",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Independent Director"
     },
     {
          "subject": "Zhao Ziye",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Independent Director"
     },
     {
          "subject": "Zhou Wen",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Supervisor"
     },
     {
          "subject": "Gao Dandan",
          "relation": "management",
          "object": "Bright Dairy & Food Co., Ltd.",
          "identity": "Employee Supervisor"
     }
];
        const colorMap = {
            "Pan Gang": "#F2A1A7",
            "Zhao Chengxia": "#7DC69B",
            "Wang Xiaogang": "#9BD7F3",
            "Lu Gang": "#FBDDDD",
            "Chaolu": "#FCE6CF",
            "Wang Yanfang": "#D5EAD9",
            "Zhao Ying": "#D8EEFB",
            "Cai Yuanming": "#DCD7EB",
            "Shi Fang": "#F2A1A7",
            "Ji Shao": "#7DC69B",
            "Chen Lang": "#9BD7F3",
            "Lu Minfang": "#FBDDDD",
            "Zhang Ping": "#FCE6CF",
            "Wen Yongping": "#D5EAD9",
            "Wang Yan": "#D8EEFB",
            "Guo Lidong": "#DCD7EB",
            "Liu Enduo": "#F2A1A7",
            "Li Xiuli": "#7DC69B",
            "Huang Liming": "#9BD7F3",
            "Ben Min": "#FBDDDD",
            "Lu Qikai": "#FCE6CF",
            "Xu Meihua": "#D5EAD9",
            "Mao Huigang": "#D8EEFB",
            "Gao Li": "#DCD7EB",
            "Zhao Ziye": "#F2A1A7",
            "Zhou Wen": "#7DC69B",
            "Gao Dandan": "#9BD7F3",
            "Inner Mongolia Yili Industrial Group Co., Ltd.": "#D8EEFB",
            "Inner Mongolia Mengniu Dairy (Group) Co., Ltd.": "#D8EEFB",
            "Bright Dairy & Food Co., Ltd.": "#D8EEFB"
        };
        // Create SVG element
        const svg = d3.select("body").append("svg")
            .attr("width", width)
            .attr("height", height);
        // Add title
svg.append("text")
    .attr("x", width / 2)
    .attr("y", 40)
    .attr("text-anchor", "middle")
    .style("font-size", "24px")
    .style("font-weight", "bold")
    .text("Knowledge Map of Dairy Management Relationships");
        // Create force simulation
        const simulation = d3.forceSimulation()
            .force("link", d3.forceLink().id(d => d.id).distance(400)) // Adjust the distance between nodes
            .force("charge", d3.forceManyBody().strength(-100)) // Adjust the repulsion force between nodes
            .force("center", d3.forceCenter(width / 2, height / 2)) // Set the center position
            .force("y", d3.forceY(height / 2).strength(0.001)); // Increase the force in the y-axis direction
        // Parse data and construct nodes and links
        const nodes = [];
        const links = [];
        data.forEach(d => {
            links.push({
                source: d.subject,
                target: d.object,
                type: d.relation
            });
            if (!nodes.find(n => n.id === d.subject)) {
                nodes.push({ id: d.subject });
            }
            if (!nodes.find(n => n.id === d.object)) {
                nodes.push({ id: d.object });
            }
        });
        // Add links (lines)
        const link = svg.append("g")
            .attr("class", "links")
            .selectAll("line")
            .data(links)
            .enter().append("line")
            .attr("class", d => "link " + d.type)
            .style("stroke", d => d.type === "management" ? "#7DC69B" : "#999");
        // Add nodes (circles)
        const node = svg.append("g")
            .attr("class", "nodes")
            .selectAll("g")
            .data(nodes)
            .enter().append("g");
        node.append("circle")
            .attr("r", 10) // Increase the radius of the nodes
            .attr("fill", d => colorMap[d.id] || "#D8EEFB"); // Use color mapping
        node.append("text")
            .attr("x", 12) // Increase the offset of the text
            .attr("y", 4)
            .text(d => d.id);
        // Set the nodes and links for the force simulation
        simulation
            .nodes(nodes)
            .on("tick", ticked);
        simulation.force("link")
            .links(links);
        // Update the positions of the nodes and links on each iteration of the force simulation
        function ticked() {
            link
                .attr("x1", d => d.source.x)
                .attr("y1", d => d.source.y)
                .attr("x2", d => d.target.x)
                .attr("y2", d => d.target.y);
            node
                .attr("transform", d => `translate(${d.x},${d.y})`);
        }
        // Mouse events
        node.on("mouseover", function(event, d) {
            link
                .transition()
                .duration(300)
                .style("stroke-opacity", l => l.source.id === d.id || l.target.id === d.id ? 1 : 0.1)
                .style("stroke-width", l => l.source.id === d.id || l.target.id === d.id ? 4 : 2); // Thicken the links
            node
                .transition()
                .duration(300)
                .attr("transform", function(o) {
                    if (o.id === d.id || links.find(l => (l.source.id === d.id && l.target.id === o.id) || (l.target.id === d.id && l.source.id === o.id))) {
                        return `translate(${o.x},${o.y}) scale(1.2)`;
                    } else {
                        return `translate(${o.x},${o.y})`;
                    }
                });
        }).on("mouseout", function() {
            link
                .transition()
                .duration(300)
                .style("stroke-opacity", 1)
                .style("stroke-width", 2); // Restore the link width
            node
                .transition()
                .duration(300)
                .attr("transform", d => `translate(${d.x},${d.y}) scale(1)`);
        });
    </script>
</body>
</html>
