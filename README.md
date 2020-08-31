# feature-preprocess
## 缺失值
np.nan,None  
### 方法
np.nansum,np.nanmin,np.nanmax,isnull,notnull,dropna(axis,how,thresh,subset),fillna(method,axis) or fillna(group的方式)  
### from sklearn.preprocessing import Imputer
1.1 Imputer(strategy,missing_values,axis)  
1.1.1 fit_transform(data),fit,transform  
## 離群值
clip(number,number)  
## 去偏態
### from scipy import stats
2.1 boxcox(data,lambda)  
## 類別變數
### 標籤化
#### from sklearn.preprocessing import LabelEncoder
3.1 LabelEncoder  
3.1.1 fit_transform(data)  
3.2 map(dict)  
### 獨熱化
4.1 astype(category)  
4.1.1 cat.codes(屬性)  
4.2 pd.get_dummies(data,prefix,columns)  
#### from sklearn.feature_extraction import DictVectorizer
4.3 DictVectorizer(sparse,dtype)  
4.3.1 fit_transform(data)  
4.3.2 get_feature_names  
#### from sklearn.preprocessing import OneHotEncoder
4.4 OneHotEncoder  
4.4.1 fit_transform(data)  
## 連續變數
### 最大最小化
#### from sklearn.preprocessing import MinMaxScaler
5.1  MinMaxScaler  
5.1.1 fit_transform(data)  
### 多項式轉換
#### from sklearn.preprocessing import PolynomialFeature
6.1 PolynomialFeatures(degree,include_bias)  
6.1.1 fit_transform(data)  
### 標準化
#### from sklearn.preprocessing import StandardScaler
7.1 StandardScaler  
7.1.1 fit_transform(data)  
### 常態化
#### from sklearn.preprocessing import Normalizer
8.1 Normalizer  
8.1.1 fit_transform(data)  
### 利用函數做轉換
#### from sklearn.preprocessing import FunctionTransformer
9.1 FunctionTransformer(function)  
9.1.1 fit_transform(data)  
## 捨棄欄位
drop(labels,axis,inplace)  
## 文字變數
### 計數
#### from sklearn.feature_extraction.text import CountVectorizer
10.1 CountVectorizer  
10.1.1  fit_transform(data)  
10.1.2 get_feature_names  
### 獨熱
#### from sklearn.feature_extraction.text import CountVectorizer
11.1 CountVectorizer  
11.1.1 fit_transform(data,binary=True)  
11.1.2 get_feature_names  
### tf-idf
#### from sklearn.feature_extraction.text import TfidfVectorizer
12.1 TfidfVectorizer  
12.1.1 fit_transform(data)  
12.1.2 get_feature_names  
## 特徵選擇
### 過濾法
13.1 corr  
#### from sklearn.feature_selection import VarianceThreshold
13.2 VarianceThreshold(threshold)  
13.2.1 fit_transform(data)  
13.2.2 fit(data)  
13.2.2.1 get_support(indices=True)  
#### from sklearn.feature_selection import SelectKBest
#### from scipy.stats import pearsonr
13.3 SelectKBest(,k)  
13.3.1 fit_transform(data)  
#### from sklearn.feature_selection import SelectKBest
#### from sklearn.feature_selection import chi2
13.4 SelectKBest(chi2,k)  
13.4.1 fit_transform(data,target)  
#### from sklearn.feature_selection import SelectKBest
#### from minepy import MINE
13.5 SelectKBest(,k)  
13.5.1 fit_transform(data)  
### 包裝法
#### from sklearn.feature_selection import RFE
14.1 RFE(estimator,n_features_to_selection)    
14.1.1 fit_transform(data,target)  
#### from sklearn.feature_selection import RFECV
14.2 RFECV(estimator, step, cv,scoring)    
14.2.1 fit (data,target)   
14.2.1.1 n_features_,grid_scores_(屬性)    
### 嵌入法
#### from sklearn.linear_model import Lasso
15.1  Lasso(alpha)  
15.1.1 fit,coef_  
#### from selection.feature_selection import SelectFromModel
15.2 SelectFromModel(estimator)  
15.2.1 fit_transform(data,target)  
*estimator:GradientBoostingClassifier,LogisticRegression(penalty="l1", C=0.1)  
*feature_importances_  
