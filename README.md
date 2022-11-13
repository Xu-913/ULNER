# ULNER
ULNER is an open source Chinese named entity recognition data set in the field of urban life.   
ULNER contains a total of 9 different entity types， 6310 train samlpes and 1305 test samples.  
ULNER是一个开源的城市生活领域下中文命名实体识别数据集。  
它包含了训练集和测试集两部分，分别包含6310和1053个样本，共计9个不同的实体类别。  

# Entity Type
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
ULNER dataset have three Generalized Entity Type which are:  
Generalized Loction, Generalized Person(similar to occupation) and Generalized Organization.  
Unlike the conventional entity types, generalized entities refer to all entities of a subclass in a conventional entity.  
Such as Bird's Nest Gymnasium and Gymnasium correspond to Loction entities and Generalized Loction entities respectively.  
ULNER数据集有两种泛化实体类型，即泛化地点和泛化人物（类似于职业）和泛化组织。  
与传统实体类型不同，泛化实体是指传统实体中的子类的所有实体。  
如鸟巢体育馆和体育馆分别对应于地点实体和泛化地点实体。  

# Colloquial Entity Type(口语化实体类型)


# Future Work
We will release ULNER2 in the following work. ULNER2 will have a larger number of samples and may have new entity categories.

# More
Research papers related to the dataset will be uploaded in the future.
