#2a)
attach(cockroft)
#2b)
boxplot(cockroft$weight~cockroft$age)
#2c)
#Berechnen Sie die Nierenclearance für jeden Patienten und fügen Sie sie
#in eine neue Spalte der Datentabelle ein, die als „Cockroft-Clearance“
#bezeichnet wird.
cockroft["Cockroft-Clearance"] <- ((140-age)*weight*1.04)/creatinin
#2d)
#Stellen Sie die bei Patienten gemessene renale Clearance gegen die 
#berechnete Clearance grafisch dar
