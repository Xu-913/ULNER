# Aims
At present, smart city has become the main development direction of each city. However, under the background of the construction of smart city assisted by artificial intelligence, there is no open source dataset available for the mainstream supervisory learning methods.  
The ULNER dataset is intended to be the first named entity recognition dataset for oral scenes in urban life to support downstream applications such as search, recommendation systems, question and answer scenarios.  
目前，智慧城市成为了目前各个城市的主要发展方向，然而在人工智能助力智慧城市的建设背景下，主流的监督学习方法尚未有相关开源的数据集可用。  
ULNER数据集目的是成为第一个城市生活领域中口语化场景的命名实体识别数据集，为下游的应用诸如：搜索、推荐系统、问答等场景提供支撑。  

# Description
ULNER is an open source Chinese named entity recognition data set in the field of urban life.   
ULNER contains a total of 9 different entity types， 6310 train samlpes and 1305 test samples.  
ULNER是一个开源的城市生活领域下中文命名实体识别数据集。  
它包含了训练集和测试集两部分，分别包含6310和1053个样本，共计9个不同的实体类别。  
The 9 entity types are:  
LOC  = Loction(地点)  
GLOC = Generalized Loction(泛化地点)  
GPER = Generalized Person(泛化人物)  
ORG  = Organization(组织)  
GORG = Generalized Organization(泛化组织)  
CCT  = Contact Information(联系方式)  
GDS  = Goods(商品)  
HBY  = Hobby(兴趣爱好)  
LCE  = Life Service(生活服务)  

# Generalized Entity Type(泛化实体类型)
ULNER dataset have three generalized entity type which are:  
Generalized Loction, Generalized Person(similar to occupation) and Generalized Organization.  
Unlike the conventional entity types, generalized entities refer to all entities of a subclass in a conventional entity.  
Such as Bird's Nest Gymnasium and Gymnasium correspond to Loction entities and Generalized Loction entities respectively.  
ULNER数据集有两种泛化实体类型，即泛化地点和泛化人物（类似于职业）和泛化组织。  
与传统实体类型不同，泛化实体是指传统实体中的子类的所有实体。  
如鸟巢体育馆和体育馆分别对应于地点实体和泛化地点实体。  

# Colloquial Entity Type(口语化实体类型)
ULNER dataset have two colloquial entity type which are:  
Hobby and Life Service.  
The order of each character may be disturbed with colloquialism, and irrelevant characters may also be inserted into each character.   
Therefore, ULNER adopts a special annotation mode for all entities.   
It records the positions of all entity characters in the sentence in the json file, rather than only the positions of the first and last characters of the entity. 
For example:  
Sentence1 = C1 C2 C3 C4 C5 C6 C7 C8, C9 C10 C11 C12 C13  
Entity1 = C7 C3, Label = [6, 2]  
Entity2 = C9 C10 C11 C12, Label = [8,9,10,11]  

ULNER数据集有两种口语实体类型，分别是：兴趣爱好和生活服务。  
各个字符的顺序可能随着口语化而被打乱，同时在各个字符中也可能插入无关字符。  
因此，ULNER对所有实体采取了特殊的标注模式，在json文件中记录了实体全部字符在句子中的位置，而不是只记录实体首尾字符的位置。例如：
Sentence1 = C1 C2 C3 C4 C5 C6 C7 C8, C9 C10 C11 C12 C13  
Entity1 = C7 C3, Label = [6, 2]  
Entity2 = C9 C10 C11 C12, Label = [8,9,10,11]  

# BaseLine
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="586" style="width:439.25pt;border-collapse:collapse;border:none;mso-border-top-alt:
 solid windowtext 1.5pt;mso-border-bottom-alt:solid windowtext 1.5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt;mso-border-insideh:
 none;mso-border-insidev:none">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;page-break-inside:avoid;
  height:55.25pt">
  <td width="109" valign="top" style="width:81.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;height:55.25pt">
  <p class="a1" style="text-indent:22.0pt"><span lang="EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">LOC<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">GLOC<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">GPER<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">ORG<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">GORG<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">CCT<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">GDS<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">HBY<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">LCE<o:p></o:p></span></p>
  </td>
  <td width="48" valign="top" style="width:35.75pt;border-top:solid windowtext 1.5pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  padding:0cm 5.4pt 0cm 5.4pt;mso-rotate:-90;height:55.25pt">
  <p class="a1" align="left" style="text-align:left;text-indent:22.0pt"><span lang="EN-US">Macro<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">Word2vec-BiLSTM-CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">75.52<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">37.32<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">58.22<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">33.93<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">49.57<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">43.63<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">38.20<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">51.42<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.44<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;mso-border-top-alt:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">57.73<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">Word2vec-BiGRU-CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">74.37<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">40.31<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">60.16<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">28.86<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.70<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">48.45<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">39.47<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.45<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">56.79<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">59.05<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">BERT-<o:p></o:p></span></p>
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span class="SpellE"><span lang="EN-US">Softmax</span></span><span lang="EN-US"><o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">85.00<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">48.48<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">69.38<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">51.31<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">61.89<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">75.29<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">47.64<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">62.31<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">64.04<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">67.90<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span class="SpellE"><span lang="EN-US">roBERTa-Softmax</span></span><span lang="EN-US"><o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">84.80<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">49.18<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">69.50<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.04<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">61.36<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">65.11<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">56.60<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">64.77<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">68.40<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.03<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">BERT-<o:p></o:p></span></p>
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">85.40<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">49.20<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">72.13<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.06<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">65.90<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">62.06<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.48<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">66.66<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">68.40<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.46<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span class="SpellE"><span lang="EN-US">roBERTa</span></span><span lang="EN-US">-<o:p></o:p></span></p>
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">86.82<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.88<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">71.86<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">50.85<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">66.66<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">65.16<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">58.46<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">66.36<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.16<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">71.90<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">BERT-<span class="SpellE">BiLSTM</span>-CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">85.38<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">51.51<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">69.53<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">48.63<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">63.84<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">61.36<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.20<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">61.35<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">65.84<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">68.73<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">BERT-<o:p></o:p></span></p>
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span class="SpellE"><span lang="EN-US">BiGRU</span></span><span lang="EN-US">-CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">86.99<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.28<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">72.01<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">51.70<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">63.58<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.73<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">51.22<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.18<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">67.62<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.91<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span class="SpellE"><span lang="EN-US">roBERTa</span></span><span lang="EN-US">-<span class="SpellE">BiLSTM</span>-CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">86.21<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.03<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">68.48<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.30<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">63.19<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">68.96<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.89<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">67.88<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">68.99<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.74<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span class="SpellE"><span lang="EN-US">roBERTa</span></span><span lang="EN-US">-<span class="SpellE">BiGRU</span>-CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">85.99<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">46.37<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">72.43<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.64<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">65.21<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">66.66<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.70<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">67.28<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">68.34<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.83<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">PERT-<o:p></o:p></span></p>
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span class="SpellE"><span lang="EN-US">Softmax</span></span><span lang="EN-US"><o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">86.82<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">47.22<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.37<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">49.81<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">63.66<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">69.66<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">52.50<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">67.85<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">68.53<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.61<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">PERT-<o:p></o:p></span></p>
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">87.09<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">56.45<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">74.61<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">57.66<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">66.09<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">61.90<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">56.65<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">67.13<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.23<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">72.70<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">PERT-<span class="SpellE">BiLSTM</span>-CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">86.81<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">49.58<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">71.30<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">53.33<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">64.09<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">71.60<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.00<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">66.22<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">67.78<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;padding:0cm 5.4pt 0cm 5.4pt;
  height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">70.80<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:14;mso-yfti-lastrow:yes;height:39.7pt">
  <td width="109" style="width:81.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">PERT-<o:p></o:p></span></p>
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span class="SpellE"><span lang="EN-US">BiGRU</span></span><span lang="EN-US">-CRF<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">87.21<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.81<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">72.60<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">55.55<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">65.15<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">76.19<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">56.67<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">67.41<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">69.97<o:p></o:p></span></p>
  </td>
  <td width="48" style="width:35.75pt;border:none;border-bottom:solid windowtext 1.5pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:39.7pt">
  <p class="a1" align="left" style="text-align:left;text-indent:0cm;mso-char-indent-count:
  0"><span lang="EN-US">72.47<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

# Future Work
We will release ULNER2 in the following work. ULNER2 will have a larger number of samples and may have new entity categories.  
接下来的工作我们将考虑扩充数据集的规模并发布ULNER2。

# More
Research papers related to the dataset will be uploaded in the future.  
相关研究论文将在发表后上传。
