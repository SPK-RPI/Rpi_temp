########################################## Syntax #####################################
############### Practical No1 ##################################################
1.Vector

 x<-c( Any data type )

2.List 

 x<-list(Anydata type )

3.Multiple vector

 x<-1:10

4.Multiple vector with steps 

 x<-seq(initial value,final value,by=step size)

5.Naming List 

 names(x)<-c(Name of individual data separatesd by ",")

6.Naming List into matrix
 
 x<-list(c(Any data type),matrix(c(Any data type),nrow=int value))

7.Merging List
 
 x<-c(First List,Second List)

8.Array
 
 x<-array(c(vector1,vector2),dim=c(int,int,int..))

9.Naming column and row
 
 x<-array(c(vector1,vector2),dim=c(int,int,int),dimnames=list(rVector,cVector,c("Matrix1","Matrix2")))

10.Assessing Arrays
 
 x[row number,colomn number,matrix number]

11.Data Frames
 
 x<-data.frame(key1=c(Any Data type),key2=c(Any Data Type),Key3=c(Any data type))

12.Build in fuctions with parameters
 
 seq(value1,value2)
 mean(value1:value2)
 sum(value1:value2)
 max(value1:value2)
 min(value1:value2)

13.Userdefind Fuctions
 
 x<-function(parameters){
    body........
 
  }

14.User defined fuctions without parameters

 x<-fuction(){
    body....

  }

15.Delete Variables

   rm(x)

############################################ Practical no2 ##############################

1.Matrix

 x<-matrix(initial element:final element,nRow,nCol,byrow=bool)

2.Nameing Matrix Elements
 
 x<-matrix(c(initial element:final element),nRow,nCol,byrow=bool,dimname=list(c(Any data type),c(Any data type)))
 
3.Transpose Matrix
  
  t(x)

4.Determinant
  
 det(x)

5.Inverse
 
 solve(x)

#####################################33 Practical No 3 ##########################3

1. Mean

 mean(vector)
 -Table 
  x<-data.frame(vector1(x),vector2(freq))
  names(x)<-c("Name1","Name2")
  y<-rep(vector1,vector2)
  mean(y)
-----------------------------------------------------------
 Llimit<-seq(from=15,to=50,by=5)
 Ulimit<-seq(from=20,to=55,by=5)
 freq<-c(9,12,16,26,14,12,6,5)
 cmark<-(Llimit+Ulimit)/2
 data<-data.frame(Llimit,Ulimit,cmark,freq)
 names(data)<-c("Lower Limit","UpperLimit","ClassMark","Frequency")
 y<-rep(cmark,freq)
 median(y)

2. Median

 meadian(vector)
 median(y)

3. Mode
 x<-c(Any data)
 mode<-function(x)
+ {
+ tab<-table(x)
+ ind<-tab[tab==max(tab)]
+ mo<-as.numeric(names(ind))
+ return(mo)
+ }
 z<-mode(x)

4.Quartile
------------------- 9th  ------ 
  x<-c(Any data)
   y<-quantile(x,0.9)
---------------- 78th --------
   y<-quantile(x,0.78)
------ All three -----
quartile(0.25,0.50,0.75,y)
IQR(y)

range=(max(y)-min(y))

5. Mean,Median with Na fuction
 
 x<-c(Any Data)
 mean(x,na=TRUE)

6. Histogram
 x<-(Any data )
 hist(x)

#################################3 Practical No4 ##############################3

1. mean,median histo,range,interquartile range
 
 x<-read.csv(file.choose(),header=T)
 attach(x)
 ------ histogram ------
 hist(x)
 ------- mean ----

################################ Practical No5 ################################

1.Standard Deviation AND Variance .csv 
  x<-read.csv(file.choose(),header=T)
  attach(x)
  var(Any colomn)
  sd(Any colomn)

################################### Practical No 6 ############################

1. chi square test
 
  x<-read.csv(file.choose(),header=T)
  attach(x)
  chisq.test(Any colomn )
 
################################## Practical No 7 #############################

1.Test of significance for single mean (Z test)
  Q. Test the hypothesis Ho:µ=10 against H1: µ≠10 random sample of the size 400 
  is drawn given mean 10.2 and Standard deviation 2.25 use 5%  level of 
  significance.
  n=400;mean=10.2;sd=2.25;mo=10                                         
  z=(mean-mo)/(sd/sqrt(n))
  
  pvalue=2*(1-pnorm(abs(z)))
  
  Since pvlaue is greater than L.O.S therefore accept the Ho at 5% level of 
  significance.
--------------------------------------------------------------------------------
2.Test of significance of difference of mean.
 Q.Two random sample of size 1000 and 2000 are drawn from 2 population 
 with same S.D 2.5 gives mean 67.5 and 68 respectively ,Test the hypothesis 
 at 5% level of significance.

n1=1000;n2=2000;sd1=2.5;sd2=2.5;x1=67.5;x2=68
z=(x1-x2)/(sqrt(((sd1^2)/n1)+(sd2^2)/n2))
pvalue=2*(1-pnorm(abs(z)))

Since pvlaue is smaller than L.O.S therefore Reject the Ho at 
5% level of significance.
---------------------------------------------------------------------------------
3.Test of significance for difference of proportion.
Q. From each of two consignment of the apple a sample of size of 200 is drawn, 
   the number of red apple counted. Test 5% of level of significance whether 
   the proportion of real apples in 2 consignment are significantly different?


 n1=200;n2=200; a=44/200;b=30/200;
 p=((n1*a)+(n2*b))/(n1+n2)
 q=1-p
 z=(a-b)/(sqrt((p*q)*((1/n1)+(1/n2))))
 pvalue=2*(1-pnorm(abs(z)))


Since pvlaue is greater than L.O.S therefore accept the Ho at 5% level of 

4.Test of significance for difference of Standard deviation.
Q.Random sample drawn from two countries gave the following data 
  related to height of adult male.


  


  
 
  

 
