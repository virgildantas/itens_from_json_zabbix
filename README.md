# itens_from_json_zabbix
create itens from json on zabbix host
1 - generate the json file, sample content: [{"ativo":1,"nome":"Disponibilidade do Banco ","data_hora":"2023-03-01 23:15:01 -0300","key":"database_id"}]
2 - generate new discovery rule on zabbix
  a - set the name, and the key, the key is more important, it will be used, "zabbix agent", update interval like you prefer.
  ![image](https://user-images.githubusercontent.com/15264944/222288992-f8403459-4902-4c8e-be6d-7aa4da2bd728.png)

  b - set LLD macros:
    b.1 - set variables to you can use on itens, "$.." i used two dots because my json needed, found the better for you, but needs start with "$."
    ![image](https://user-images.githubusercontent.com/15264944/222289172-cc4cd62d-9908-4118-b837-3b6c215faad9.png)
    
  c - on new Item prototype set name with variable you are setted before. Confirme type off return value, update interval.
  ![image](https://user-images.githubusercontent.com/15264944/222289441-a5bb3b86-8c41-4235-b9b8-949467801667.png)

  d - on Preprocessing, you will set the keys to you can use, respecting the prefix off item b.1.
  ![image](https://user-images.githubusercontent.com/15264944/222289646-d9efa604-fbc6-4479-a04c-ccdae0c1dd1b.png)

  e - set the triggers you identify you are needed.
  ![image](https://user-images.githubusercontent.com/15264944/222289706-75c878ae-c1a1-4aa7-8604-2ef7044446f0.png)
