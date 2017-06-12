# Line Bot Example

1. 從政府的統計資訊網 http://statdb.dgbas.gov.tw/pxweb/Dialog/statfile9.asp 下載 __家庭收支-平均每戶全年經常性支出__ 的統計資料。

	![expense](https://github.com/104corp/2017-104Hackathon-AppWebService/blob/master/linebot-example/expense.png)


2. 整理[結構化的職務資料集](https://github.com/104corp/2017-104Hackathon-AppWebService/blob/master/sample-data/job_structured_info_sample.csv) 的jobcat1, jobcat2, jobcat3, salary-low, salary-high, role, addr-no等欄位，統計出每個地區每個職務類別的全職平均年薪，並與第一項的家庭年支出計算收入支出的差後產生結果。

3. 將結果中的代碼對照類目表的文字，職務代碼利用[職務類目](https://github.com/104corp/2017-104Hackathon-AppWebService/blob/master/sample-data/job_category_sample.csv); 地區代碼利用[地區類目](https://github.com/104corp/2017-104Hackathon-AppWebService/blob/master/sample-data/district_sample.csv)。

	![result](https://github.com/104corp/2017-104Hackathon-AppWebService/blob/master/linebot-example/result.png)


4. 利用同一個資料集裡的job, jobcat1, jobcat2, jobcat3與facebook opensource的[fasttext text classification](https://github.com/facebookresearch/fastText)，訓練一個職務名稱的分類模型，讓使用者輸入職務名稱時可以對應到職務分類(ex. 會計 -> 記帳/出納/會計)。

	

5. 將結果與分類模型整合，與Line或Facebook Messenger的bot api串接，就可以完成一個簡單的聊天機器人查詢的應用。

<img src="https://github.com/104corp/2017-104Hackathon-AppWebService/blob/master/linebot-example/line_screenshot.png"  width="50%">
