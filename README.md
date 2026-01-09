1 Install on Windows

bin\wget https://mirrors.aliyun.com/python-release/windows/python-3.12.10-amd64.exe

C:\Users\Administrator\AppData\Local\Programs\Python\Python312\Scripts\pip install -i https://mirrors.aliyun.com/pypi/simple pywencai

bin\wget https://nodejs.org/download/release/v16.20.2/node-v16.20.2-x64.msi

2 Run inside Python

import pywencai

res = pywencai.get(query='退市股票', sort_key='退市@退市日期', sort_order='asc')
#res = pywencai.get(query='年内跌幅大于60%，obv周线大于0', query_type='usstock')
#res = pywencai.get(query='停牌股票', query_type='hkstock', loop=True) #一个月停牌
#print(res)

#res = pywencai.get(query='一月跌幅大于7%，一周跌幅大于4%', query_type='fund', loop=True)
#res = pywencai.get(query='年内跌幅大于60%，obv周线大于0', query_type='usstock')
#print(res)

3 Parameters for pywencai
3.1 query

3.2 query_type
取值	含义
stock	股票
zhishu	指数
fund	基金
hkstock	港股
usstock	美股
threeboard	新三板
conbond	可转债
insurance	保险
futures	期货
lccp	理财
foreign_exchange	外汇

3.3 sort_key
