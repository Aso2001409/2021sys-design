```uml
@startuml
start
:weather;
if(weather=0)then(Yes)
  :快晴です;
else if(weather=1)then(Yes)
  :曇りです;
else if(weather=2)then(Yes)
  :雨です;
else(No)
  :不明です;
endif
end
@enduml
```
