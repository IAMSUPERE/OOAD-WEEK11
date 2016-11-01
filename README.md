# OOAD-WEEK11
State Diagram

ข้อ1
```
@startuml

Title one day one life
State "Wake Up" as wakeup
State "Eating Breakfest" as eatingbreakfest
State "Go to school" as gotoschool
State "Eating Lunch" as eatinglunch
State "Have a study" as haveastudy
State "Dinner Time" as dinnertime
State "Sleep" as sleep

wakeup -right-> eatingbreakfest
eatingbreakfest -> gotoschool
gotoschool -> eatinglunch
eatinglunch -> haveastudy
haveastudy -down-> dinnertime
dinnertime -left-> sleep
sleep -up-> wakeup

@enduml
```
![](http://www.plantuml.com/plantuml/img/PP71RWCX34JlVCKeTtwXYgfMxQ6tfChP3TvT50AhnJJAtvU5qaNf1MRiXpKM-oYqIBewfOvM72DuXg5xkPqTM1s4XB4xqONnEUz04RUiqzmwhoJMZtXUc2u3Hoa8b-9NgpNsBK02udaAmHLk31AgVHZtaVnvwaQvrJVcdRuPX2Z9t0ipvG8Lsv0NwpqlEDeh5y8KBzasuk2OwpvnLKhLjQ0NEqwYd_xjyE2HaIx-9l7tjeRkzDhgicuIseIRpzqkvoQX7Gzhf9gqdD1fpfNVlr1xzYP_umy0)

ข้อ2
```
@startuml

title Final Test

State Book
State Teacher
State Test

[*] -right-> Book : Read
Book -down-> Test : Do
Test -left-> Teacher : Pass

@enduml
```
![](http://www.plantuml.com/plantuml/img/FOun2iCm34LtdK9pmHV8K489dKkRhMGGjTgOk3ROF-JwTKJ9zgJt4Eehf63zHY84HELhI19vr0gY1mJAbvoNFuughrdBCUtHypInA-4pmvsjvOxlAfwCdSzRQc9lcnWo6RceRzZQ3ZPparg9Uas-FVC3)

ข้อ3
```
@startuml

title School
[*] -down-> School

State School{
  State Student
  State Teacher
  State Book
  State Class
  State Test
  
  Teacher --> Test : create
  Student --> Book : read
  Student -up-> Test : do
  Teacher --> Student : teach
  Teacher --> Class : have
  Student -up-> Class : in
}  
@enduml
```
![](http://www.plantuml.com/plantuml/img/PP113i8W44Ntd6BM9boW2zFe4UhEk21b4XgHCJ3emiixa89DJTZyUV__cJ0cDf7pmol52tk4QNP4NbqFDz2Mta4VsqXDRBWPFWfWrPmj1kxwWcPs6Bi-4TsxE7kJqiQQIaxU6W8jwyeK1fWZYgTwwuBAIfamGNPBylENixJhQwu1k4ntj5uap9aN_bKsk8HoveZ1oazz0G00)

ข้อ4
```
@startuml

title School
[*] -down-> School

State School{
  State Student1
  State Teacher
  State Book
  State Class
  State Test
  
  Teacher --> Test : create
  Student1 --> Book : read
  Student1 -up-> Test : do
  Teacher --> Student1 : teach
  Teacher --> Class : have
  Student1 -up-> Class : in
}  
School -> University : Test

State University{
  
  Student2 --> Sheet : read
  Student2 --> Midterm : do
  Student2 --> Final : do
  Professor --> Midterm : create
  Professor --> Final : create
  Professor --> Student2 : instructive
} 
@enduml
```
![](http://www.plantuml.com/plantuml/img/TP8z2y8m48Rt_8gRXGuwEeWek0c2Eeb3Q4uQZ8aaLqN4_-wrQQAj25dkdlS-tYFpGD9JVJ52a2Q3i2qhvumuZ8vGA7UtnIobn9Oa9S5J07GnrGejZNDYXxAiqETuuTmv1qiZG_YI1kA0NrS41SzhiZ25qYDhMcsSqCAc6qDcgeVgwwTIkK77B9i2DUa1RfTYLiaR_ZPDL5lnubsZVs2mj_g6FcXwC6sjT2VwW6TqrtMSn6KgHFgn4DbQAq9_IHvwRAMjD8bil3jX2CuFolBH-e9K-mVdEOtBGBukYHsmNJ57g_Xtl040)

ข้อ5
```
@startuml

title Computer
[*] -> Computer

State Computer{
  State CPU{  
    PC --> Mem
    PC --> Mux
    Mem --> Control
    Mem --> PC
    Control --> Mem
    Control --> Mux
    Control --> Mult
    Control --> Shifter
    Control --> ALU
    Control --> PC
    Control --> Register
    Register --> Mux
    Register --> Mem
    Mux --> Mult
    Mux --> ALU
    Mux --> Shifter
    Shifter --> Mux
    Shifter --> Mem
    Shifter --> PC
    
  }
  State RAM
  
  CPU --> RAM
  RAM --> CPU
}
 
@enduml
```
![](http://www.plantuml.com/plantuml/img/RP712eCm38RlUOgS1xx2K7gTK1HFOmTXtIPK7HfX87ltPJMTPjibzF_I97-RTAHweAdr0DIGTsZwzZwH6-2uEs6oNpMKLDEQdm5HYArcH9Q8rc32DRbhbPmUGJ8EslGT3RrNp9eW9QMwA2QjDFFq0yjRStcx_kRPeVfXVsONxjgCiJuAvK13iSf9RIc2E3RghJqvg-wAIVCj4yiSdfyz55aE0V52baS4m77vTLi1NuRKTMVUzmi0)
