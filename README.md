# 论文检索与解析工具 

一个基于arXiv的论文检索与内容解析工具，支持论文搜索、PDF链接获取和内容解析功能，适用于学术研究和AI领域的最新论文获取。
A paper retrieval and content parsing tool based on arXiv, supporting paper search, PDF link retrieval, and content parsing functions, suitable for obtaining the latest papers in academic research and AI fields.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| search_arxiv | 搜索 arXiv 论文 |
| get_recent_ai_papers | 获取 arXiv AI 领域最新论文（cs.AI/recent） |
| get_arxiv_pdf_url | 获取 arXiv PDF 下载链接 |
| parse_paper_content | 解析论文内容（优先使用 HTML 版本，回退到 PDF） |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659949571](https://mcp.xiaobenyang.com/inspector/1777316659949571)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659949571](https://mcp.xiaobenyang.com/inspector/1777316659949571)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "论文检索与解析工具": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659949571/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "论文检索与解析工具": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659949571/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "论文检索与解析工具": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659949571",
          },
          "transport": "stdio"
        }
      }
}

```
