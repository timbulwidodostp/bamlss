# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Fit Bayesian Additive Models for Location Scale and Shape (and Beyond) Use bamlss With (In) R Software
install.packages("bamlss")
library("bamlss")
bamlss = read.csv("https://raw.githubusercontent.com/timbulwidodostp/bamlss/main/bamlss/bamlss.csv",sep = ";")
# Estimation Fit Bayesian Additive Models for Location Scale and Shape (and Beyond) Use bamlss With (In) R Software
f <- num ~ s(x1) + s(x2) + s(x3) + te(lon, lat)
bamlss <- bamlss(f, data = bamlss, optimizer = opt_bfit, sampler = FALSE)
print(bamlss)
summary(bamlss)
bamlss <- bamlss(f, data = bamlss, start = coef(b1), optimizer = FALSE, sampler = sam_GMCMC)
print(bamlss)
summary(bamlss)
# Fit Bayesian Additive Models for Location Scale and Shape (and Beyond) Use bamlss With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished