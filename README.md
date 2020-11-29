# R-限行分析
library(readxl)
xianxing<-read_excel("xianxing2.xlsx")
#AQI
plot(xianxing$time,xianxing$AQI2017yin,type='o',lty=5,lwd=2,pch=0,col=4,ylim = c(0,400),
     xlab=NA,ylab=NA,xaxt='n',yaxt='n')
par(new=T)
mtext(text='t(days,日)',side=1,line=1.5)
mtext(text='AQI(Air Quality Index,空气质量指数)',side=2,line=2)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(mgp=c(2.5,0.5,0))#可用于调整刻度数值与坐标轴的距离远近
par(new=T)
month<-paste(12,28,sep="/")
axis(1,tcl=0.25,,las=1,at=28,labels=month) 
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=50,length=9))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=50,length=9),labels = NA)
lines(xianxing$time,xianxing$AQI2016yin,type='o',lty=1,lwd=2,pch=1,col=3,)
lines(xianxing$time,xianxing$AQI2017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$AQI2016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topleft',legend=c('AQI of Yinchuan 2017','AQI of Yinchuan 2016','AQI of Wuzhong 2017','AQI of Wuzhong 2016'),
       lty=c(5,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)


#PM2.5
plot(xianxing$time,xianxing$PM2.52017yin,type='o',lty=5,lwd=2,pch=0,col=4,ylim = c(0,220),
     xlab=NA,ylab=NA,xaxt='n',yaxt='n')
par(new=T)
mtext(text='t(days,日)',side=1,line=1.5)
mtext(text='PM2.5浓度',side=2,line=2)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(mgp=c(2.5,0.5,0))#可用于调整刻度数值与坐标轴的距离远近
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=20,length=12))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=20,length=12),labels = NA)
lines(xianxing$time,xianxing$PM2.52016yin,type='o',lty=1,lwd=2,pch=1,col=3,)
lines(xianxing$time,xianxing$PM2.52017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$PM2.52016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topright',legend=c('PM2.5 of Yinchuan 2017','PM2.5 of Yinchuan 2016','PM2.5 of Wuzhong 2017','PM2.5 of Wuzhong 2016'),
       lty=c(5,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)

#PM10
plot(xianxing$time,xianxing$PM102017yin,type='o',lty=5,lwd=2,pch=0,col=4,ylim = c(0,500),
     xlab=NA,ylab=NA,xaxt='n',yaxt='n')
par(new=T)
mtext(text='t(days,日)',side=1,line=1.5)
mtext(text='PM10浓度',side=2,line=2)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(mgp=c(2.5,0.5,0))#可用于调整刻度数值与坐标轴的距离远近
par(new=T)
month<-paste(12,28,sep="/")
axis(1,tcl=0.25,,las=1,at=28,labels=month) 
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=50,length=11))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=50,length=11),labels = NA)
lines(xianxing$time,xianxing$PM102016yin,type='o',lty=1,lwd=2,pch=1,col=3,)
lines(xianxing$time,xianxing$PM102017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$PM102016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topleft',legend=c('PM10 of Yinchuan 2017','PM10 of Yinchuan 2016','PM10 of Wuzhong 2017','PM10 of Wuzhong 2016'),
       lty=c(5,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)


#SO2
plot(xianxing$time,xianxing$SO22017yin,type='o',lty=5,lwd=2,pch=0,col=4,ylim = c(0,200),
     xlab=NA,ylab=NA,xaxt='n',yaxt='n')
par(new=T)
mtext(text='t(days,日)',side=1,line=1.5)
mtext(text='SO2浓度',side=2,line=2)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(mgp=c(2.5,0.5,0))#可用于调整刻度数值与坐标轴的距离远近
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=20,length=13))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=20,length=13),labels = NA)
lines(xianxing$time,xianxing$SO22016yin,type='o',lty=1,lwd=2,pch=1,col=3,)
lines(xianxing$time,xianxing$SO22017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$SO22016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topleft',legend=c('SO2 of Yinchuan 2017','SO2 of Yinchuan 2016','SO2 of Wuzhong 2017','SO2 of Wuzhong 2016'),
       lty=c(5,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)

#CO
plot(xianxing$time,xianxing$CO2017yin,type='o',lty=5,lwd=2,pch=0,col=4,ylim = c(0,5),
     xlab=NA,ylab=NA,xaxt='n',yaxt='n')
par(new=T)
mtext(text='t(days,日)',side=1,line=1.5)
mtext(text='CO浓度',side=2,line=1.5)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(mgp=c(2.5,0.5,0))#可用于调整刻度数值与坐标轴的距离远近
par(new=T)
month<-paste(12,12,sep="/")
axis(1,tcl=0.25,las=1,at=12,labels=month) 
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=1,length=6))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=1,length=6),labels = NA)
lines(xianxing$time,xianxing$CO2016yin,type='o',lty=1,lwd=2,pch=1,col=3)
lines(xianxing$time,xianxing$CO2017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$CO2016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topright',legend=c('CO of Yinchuan 2017','CO of Yinchuan 2016','CO of Wuzhong 2017','CO of Wuzhong 2016'),
       lty=c(5,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)

#NO2
plot(xianxing$time,xianxing$NO22017yin,type='o',lty=5,lwd=2,pch=0,col=4,ylim = c(0,110),
     xlab=NA,ylab=NA,xaxt='n',yaxt='n')
par(new=T)
mtext(text='t(days,日)',side=1,line=1.5)
mtext(text='NO2浓度',side=2,line=2)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(mgp=c(2.5,0.5,0))#可用于调整刻度数值与坐标轴的距离远近
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=10,length=12))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=10,length=12),labels = NA)
lines(xianxing$time,xianxing$NO22016yin,type='o',lty=1,lwd=2,pch=1,col=3)
lines(xianxing$time,xianxing$NO22017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$NO22016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topleft',legend=c('NO2 of Yinchuan 2017','NO2 of Yinchuan 2016','NO2 of Wuzhong 2017','NO2 of Wuzhong 2016'),
       lty=c(5,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)

#O3_8h
plot(xianxing$time,xianxing$O3_8h2017yin,type='o',lty=5,lwd=2,pch=0,col=4,ylim = c(0,100),
     xlab=NA,ylab=NA,xaxt='n',yaxt='n')
par(new=T)
mtext(text='t(days,日)',side=1,line=1.5)
mtext(text='O3_8h浓度',side=2,line=2)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(mgp=c(2.5,0.5,0))#可用于调整刻度数值与坐标轴的距离远近
par(new=T)
month<-paste(12,23,sep="/")
axis(1,tcl=0.25,las=1,at=23,labels=month)
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=10,length=11))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=10,length=11),labels = NA)
lines(xianxing$time,xianxing$O3_8h2016yin,type='o',lty=1,lwd=2,pch=1,col=3)
lines(xianxing$time,xianxing$O3_8h2017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$O3_8h2016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topleft',legend=c('O3_8h of Yinchuan 2017','O3_8h of Yinchuan 2016','O3_8h of Wuzhong 2017','O3_8h of Wuzhong 2016'),
       lty=c(5,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)



library(ggplot2)      
library(readxl)
xianxing<-read_excel("xianxing2.xlsx")
ggplot(xianxing,aes(x=time,y=PM2.52017yin))+geom_line(color='blue',size=1)







plot(xianxing$time,xianxing$AQI2017yin,type='o',lty=2,lwd=2,pch=0,col=4,ylim = c(0,400),
     xlab='t(days,日)',ylab='AQI(Air Quality Index,空气质量指数)',xaxt='NA',yaxt='NA',mgp=c(2,0.5,0),las=1,tcl=0.25)
par(new=T)

mtext(text=,side=1,line=2)
mtext(text=,side=2,line=2.5)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(new=T)
month<-paste(12,28,sep="/")
axis(1,tcl=0.25,,las=1,at=28,labels=month) 
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=50,length=9))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=50,length=9),labels = NA)
lines(xianxing$time,xianxing$AQI2016yin,type='o',lty=1,lwd=2,pch=1,col=3)
lines(xianxing$time,xianxing$AQI2017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$AQI2016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topleft',legend=c('AQI of Yinchuan 2017','AQI of Yinchuan 2016','AQI of Wuzhong 2017','AQI of Wuzhong 2016'),
       lty=c(2,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)


plot(xianxing$time,xianxing$AQI2017yin,type='o',lty=2,lwd=2,pch=0,col=4,ylim = c(0,400),
     xlab=NA,ylab=NA,xaxt='n',yaxt='n')
par(new=T)

mtext(text='t(days,日)',side=1,line=2)
mtext(text='AQI(Air Quality Index,空气质量指数)',side=2,line=2.5)
month<-paste(12,seq(from=10,by=5,length=5),sep="/")
axis(1,tcl=0.25,,las=1,at=seq(from=10,by=5,length=5),labels=month) 
par(new=T)
month<-paste(12,28,sep="/")
axis(1,tcl=0.25,,las=1,at=28,labels=month) 
axis(side=2,tcl=0.25,las=1,at=seq(from=0,by=50,length=9))
axis(side=3,tcl=0.25,las=1,at=seq(from=10,by=5,length=5),labels = NA)
axis(side=4,tcl=0.25,las=1,at=seq(from=0,by=50,length=9),labels = NA)
lines(xianxing$time,xianxing$AQI2016yin,type='o',lty=1,lwd=2,pch=1,col=3)
lines(xianxing$time,xianxing$AQI2017wu,type='o',lty=1,lwd=2,pch=5,col=2)
lines(xianxing$time,xianxing$AQI2016wu,type='o',lty=1,lwd=2,pch=13,col=6)
legend('topleft',legend=c('AQI of Yinchuan 2017','AQI of Yinchuan 2016','AQI of Wuzhong 2017','AQI of Wuzhong 2016'),
       lty=c(2,1,1,1),bty='n',col=c(4,3,2,6),pch=c(0,1,5,13),lwd=2)
