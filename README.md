# Задания на python




--------------------------------------------------   PYTHON ------------------------------------------   

```
input_str = """ Андрей 9
  Василий 11
  Роман 7
  X Æ A-12 45
  Иван Петров 3
  ..
  Андрей 6
  Роман 1
  ....
"""
stats = {}
lines = input_str.split('\n')

for line in lines:
    if line == '..' or line == '':
        continue
    hour = ' '.join(line.split()[-1:])
    name = line[:-2].strip()
    if name not in stats:
        stats[name] = []
    stats[name].append(hour)

for name, hours_list in stats.items():
    count = 0
    for x in hours_list:
        count += int(x[0])
    print(f"{name}: {', '.join(str(x) for x in hours_list)} ; sum: {count}")
    count = 0
    
    
#while True:
    #input_str = input()
    #if not input_str:
       # break

    #name, hours = input_str.split()
    #if name not in stats:
        #stats[name] = []
    #stats[name].append(int(hours))

#for name, hours_list in hours_dict.items():
   # print(f"{name}: {', '.join(map(str, hours_list))}; sum: {sum(hours_list)}")
    
    
```
    
-----------------------------------------------------     SQL     ------------------------------------------        

```
SELECT article.id, article.title
FROM article
LEFT JOIN comment ON article.id = comment.article_id
WHERE comment.article_id IS NULL;
```
    
