# DATA-SCIENCE_DEEP-LEARNING_NOTES

## AI Deep Learning -- RANDOM_NOTE: 

##一般常見的聯合學習框架##: 
  # Google的Tensorflow Federated、臉書的PySyft、Nvidia的Clara、百度的Paddle Federated Learning（PFL）, 及中國純網銀微眾銀行的FATE
  # TW: AI Lab, Harmonia: 採用工程師熟悉的環境和語言，如熱門的開源工具Kubernetes, Git Large File Storage,和GitOps

 #具體應用場景: 聯合學習醫療聯盟
  ##def: 聯盟的運作，會由各領域專家提出聯合學習協定，先行訓練出一套聯合學習樣板AI模型後，再邀請有意願的醫療單位加入，以各自的資料在端點訓練模型
  ##EG: Google在2017年發表的研究成果，就是聯合學習的經典案例。
      ##當時，Google為改善手機虛擬鍵盤輸入程式Gboard的選字建議，但又不想收集每位用戶的使用資料，於是設計一套分散式機器學習方法，讓每支手機從中央主機下載一套模型，在用戶端依使用者行為，來訓練Local端模型。
      ##訓練好後，用戶手機會上傳模型權重至中央主機，中央主機收集一定數量的權重後，就會聚合（Aggregation），計算出一個優化過的權重，再回放到用戶端手機，進行下一輪訓練。後來，Google就將這套多次優化的模型，部署到數百萬支Android手機上。


### 關聯規則 ###	  
#1 支援程度 Suport：就是某物品的出現次數，佔所有記錄條數的比例 (%)
   
#2 信賴程度 Confidence：A事件出現的次數為 m1， A和B事件同時出現的次數為 m2， 那麼A事件發生之後，B事件也有可能發生的自信度為：m2/m1	  
   #如果自信度越高，表示兩者的關聯性越強。也就是A事件發生，B事件也很可能也會發生
   
#3 興趣度interest：關聯規則有 A -> B, 表示A事件發生，B事件也發生的情況。
  #它們的自信度為c， B事件的支援度為s，那麼B事件的興趣度為（c - s）.
  #如果 B相對於A的自信度(C)很高，表示兩者的關聯性很強; s很低，表示產品B在購物清單中不常見，也就是C和S相差越大，則insterest的值就越大。
       # 那A和B之間的關聯性很可能就是我們所感興趣的。
  # 如果A表示牛奶，B表示麵包，那麼他們的自信度c會很大，B的s也很大，所以（c-s）的值相差不大 => 因此就不會是我們所感興趣的了



### Apriori演算法 ##
  # 如果某個項不是頻繁項，那麼所有包含它的項都不是頻繁項。什麼意思？
  # 舉例：比如{A}, {A, B}, 如果{A}的支援度為0.4， 那麼{A, B}的支援度不可能大於0.4.
          #所以，如果A不是頻繁項，那麼{A，B}這兩個元素所構成的項也不是頻繁項。    
  # 相反，只有上一級是頻繁項的情況下，下一級的項才有可能是頻繁項。如上面圖片虛線部分所示	  
  # 相比於前面的普通演算法，Apriori演算法能夠根據前面的計算大量減少了記憶體空間的消耗。  


  
### PCV演算法 ###  
  
  
  
### TERMS: AI組織人工智慧全球夥伴聯盟（GPAI）
### PCV演算法 
