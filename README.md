
<h2 align="center">chinese-daoism: 一个中国道教经典数据库</h2>

## 简介

《道藏》者，道教一切经书之总集也。夫生天地，和阴阳，包囊万物，亘古不易者，道也；弘道德，正纪纲，成就仙业，利乐群生者，教也。总而谓之曰经，聚之于室曰藏。诵经者足以劝善植福，聚藏者足以积德累功。仙真圣人所以美教化，移风俗，自度而度人者，莫不以经教为津梁也。

## 数据格式

### 对于单独的经文(文件名为 <经文名>.json)

##### 示例 : json/三洞真经/洞真上清经/真诰.json

```json
{
    "title": "真诰",
    "description": "经名：真诰，收录于《中华道藏》洞真上清经。",
    "paragraphs": [
        "真诰卷之一",
        "金阙右卿司命蓬莱都水监梁国师贞白真人华阳隐居陶弘景造",
        "..."
    ]
}
```

### 对于原来分为多个章节的经文(文件名为 <经文名>_multi.json)

##### 示例 : json/三洞真经/洞真上清经/上清大洞真经_multi.json

```json
{
    "title": "上清大洞真经",
    "description": "经名：上清大洞真经，收录于《中华道藏》洞真上清经。",
    "chapters": [
        {
            "index": 1,  //章节编号不一定从1开始且不一定连续！
            "paragraphs": [
                "诵经玉诀",
                "...."
            ]
        },
        {
            "index":2,
            "paragraphs":[
                "....",
                "...."
            ]
        }
    ]
}
```

## 贡献

这个数据库中几乎所有数据都来自[道人家](www.daorenjia.com)，我使用了采集软件抓取这个网站，之后使用Node.js脚本将网页转换为json文件。这个行为已经过站长许可。  
你可以直接前往这个网站进行数据的新增/勘误，也可以提交pull request，我会将改动反馈回原网站。  
本仓库会和网站不定期进行同步。  
当然，这个仓库的文件中有可能存在很多相似的问题，这很可能是转换脚本的缺陷所导致。假设是这种情况，你应该优先考虑改进转换脚本。  
***这个仓库的内容仍然存在非常多的错误，敬请谅解！***
