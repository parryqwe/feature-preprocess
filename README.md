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
4.2 pd.get_dummies(data,prefix)
#### from sklearn.feature_extraction import DictVectorizer
4.3 DictVectorizer(sparse,dtype)
4.3.1 fit_transform(data)
4.3.2 get_feature_names
#### from sklearn.preprocessing import OneHotEncoder
4.4 OneHotEncoder
4.4.1 fit_transform(data)
## 連續變數
### 最大最小化
5.1  MinMaxScaler
5.1.1 fit_transform(data)
