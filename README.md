# ShinyappUE
Code for UE shiny app

Link to server: http://actuaryserver:3942

Dates in ClaimBin file should be formatted 01/01/16 in the csv 

#add words
dtm_mat<-as.matrix(inspect(dtm[,c("gay","lesbian","gender","lgbt","ident","transgend","stereotyp","homosexu","transsexu")]))
dtm_mat2<-cbind(mydata$Claim.Number,dtm_mat)
claiminfo2<-aggregate(dtm_mat2[,2:2480], by=list(Category=dtm_mat2[,1]), FUN=sum)
#make sure to replace all values greater than zero as one
