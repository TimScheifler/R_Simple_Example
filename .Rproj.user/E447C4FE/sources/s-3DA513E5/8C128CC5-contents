perecent_survived = (nb_plants_survived / nb_plants * 100)
herbicides["perecent_survived"] = perecent_survived
sum(perecent_survived < 5)
#Aufgabe e)
#Erstelle "control" f?r jene die in herbicides geh?ren (?)
control <- herbicides[herbicides["herbicide"]=="none",]


#Aufgabe f)
#Berechne den Durchschnitt Anzahl an Pflanzen 97
Control_Mittelwert <- mean(control$perecent_survived)#93,75

#Berechne deren Standartabweichung 4,74
Control_Standartabweichung <- sd(control$perecent_survived)#4,74

#Aufgabe g)

#Mittelwert
mean(herbicides[which(herbicide=="herbicide1"),"perecent_survived"])#61.66904
mean(herbicides[which(herbicide=="herbicide2"),"perecent_survived"])#55.96954
mean(herbicides[which(herbicide=="herbicide3"),"perecent_survived"])#11.17945

#Standardabweichung
sd(herbicides[which(herbicide=="herbicide1"),"perecent_survived"])#32.31872
sd(herbicides[which(herbicide=="herbicide2"),"perecent_survived"])#25.89133
sd(herbicides[which(herbicide=="herbicide3"),"perecent_survived"])#7.919575

attach(herbicides)
#Aufgabe h)
#Welche Pflanze ist insgesamt am resistentesten gegen Herbizide?
resistence_corn = mean(herbicides[which(plant == "corn" & herbicide!="none"), "perecent_survived"])#56.76
resistence_grass = mean(herbicides[which(plant == "grass" & herbicide!="none"), "perecent_survived"])#35.68

resistence_grass = mean(subset(perecent_survived, plant == "grass" & herbicide!="none"))#35.68
resistence_potatoe = mean(herbicides[which(plant == "potatoe" & herbicide!="none"), "perecent_survived"])#36.37

#Aufgabe i)
#Was sind die Variablen in dieser Studie? Welchen Typ haben sie?

#Aufgabe j)
temp_var = herbicides[which(herbicide!="none"), "perecent_survived"]
#Zeichnen Sie ein stripchart, das die Rate der überlebenden Pflanzen darstellt.
stripchart(temp_var, method = "stack")

#Aufgabe k)
#Zeichnen Sie ein Histogramm, das die Rate der überlebenden Pflanzen darstellt. Welches Diagramm ist Ihrer Meinung nach besser lesbar: das Streudiagramm (stripchart) oder das Histogramm?
hist(temp_var)
#Das Histogram eignet sich eher, da man eine präzisere Darstellung der Häufigkeit ablesen kann. Dies eignet sich vor allem bei vielen Werten.

#Aufgabe l)
#Zeichnen Sie ein Kreisdiagramm (piechart), das den Anteil der verschiedenen Pflanzen in der Studie darstellt.
pie(summary(as.factor(herbicides[which(herbicide!="none"), "plant"])))

#Aufgabe m)
#Zeichnen Sie ein Diagramm, das die Überlebensrate als Funktion der Pflanzenarten darstellt. 
#Welche Art ist insgesamt am besten gegen alle drei Herbizide resistent?
boxplot(herbicides[which(herbicide!="none"),"perecent_survived"]~herbicides[which(herbicide!="none"), "plant"])

#Aufgabe n)
boxplot(herbicides[which(herbicide!="none"),"perecent_survived"]~herbicides[which(herbicide!="none"), "herbicide"])

#Aufgabe o)
plants <- herbicides[herbicides["herbicide"]!="none",]
boxplot(plants$perecent_survived~plants$plant:plants$herbicide)

#Aufgabe p)
#Beantworten Sie folgenden Fragen anhand der vorherigen Abbildungen:
#  a. Welches Herbizid eignet sich am besten für die Anwendung auf
#Straßen, auf denen keine Pflanzen wachsen sollen?
# Herbicide 3 eignet sich am besten für die Anwendung auf Straßen, auf denen keine Pflanzen wachsen sollen.
# Die niedrigste Überlebensrate aller Pflanzen wird bei Herbicide 3 erreicht, was aus dem Boxplot der Aufgaben "n" und "o" abgelesen werden kann.

#  b. Welches Herbizid eignet sich am besten für die Anwendung auf
#einem Maisfeld, auf dem Mais wachsen soll, Gras und Kartoffeln
#jedoch nicht?
# Herbicide 1, weil bei diesem der Mais die höchste Überlebensrate hat, wobei diese nur minimal höher als bei Herbicide 2 ist.

#  c. Welches Experiment kann in Betracht gezogen werden, um die
#Behandlungseffizienz dieses Maisfeldes zu verbessern?
#Man sollte Herbicide 1 & 2 mischen, weil Mais unter deren Auswirkungen nicht besonders leidet.
