# Venn-diagram-showing-understory-species-count-in-each-overstory-type
Venn diagrams in ggplot showing understory species count in each overstory type

####Venn diagram for species ditribution for invasive####
data<-read.csv("~/Desktop/iiser/8 sem/Vegetation paper/2017_only_nilgiri_anamalai_palani/Distribution of species in pure euc, aca, pine1.csv")
str(data)

colnames(data)[1]<-"Pinus"

Acacia <- data$Acacia[data$Acacia!=""]
Eucalyptus <- data$Eucalyptus[data$Eucalyptus!=""]
Pinus <- data$Pinus[data$Pinus!=""]

D<- list(Acacia=Acacia ,Eucalyptus=Eucalyptus ,Pinus=Pinus )

library(ggvenn)
ggvenn(D, 
       fill_color = c( "#0073C2FF", "#EFC000FF", "#868686FF"),
       stroke_size = 0, set_name_size = 6, fill_alpha = 0.3, text_color = "black", text_size = 8, show_percentage = FALSE
)

####Venn diagram for species ditribution for shola####
data<-read.csv("~/Desktop/iiser/8 sem/Vegetation paper/2017_only_nilgiri_anamalai_palani/Distribution of shola spp in diff stands.csv")
str(data)

Acacia <- data$Acacia[data$Acacia!="0"]
Eucalyptus <- data$Eucalyptus[data$Eucalyptus!="0"]
Pine <- data$Pine[data$Pine!="0"]

D<- list(Acacia=Acacia ,Eucalyptus=Eucalyptus ,Pine=Pine )

library(ggvenn)
ggvenn(D, 
       fill_color = c( "#0073C2FF", "#EFC000FF", "#868686FF"),
       stroke_size = 0, set_name_size = 6, fill_alpha = 0.3, text_color = "black", text_size = 8, show_percentage = FALSE
)


