# 객체

### 객체의 생성

```javascript
var grades = new Object(); // 내장 생성자 함수 
grades['egoing'] = 10;
grades['k8805'] = 6;
grades['sorialgi'] = 80;

var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
```

```javascript
// key : value
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
alert(grades['sorialgi']); // ['sorialgi'], return : 80
alert(grades.sorialgi); // .sorialgi, return : 80
```

**for in문** 

```javascript
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
for(key in grades) { 
    document.write("key : " + key + ", value : " + grades[key] + "<br />");
}

/*
    key :   egoing, value : 10
    key :   k8805, value : 6
    key :   sorialgi, value : 80
*/
```

**객체에는 객체를 담거나 함수를 담을 수 있음**

```javascript
// 객체 지향 프로그래밍 기법
var grades = {
    'list': {'egoing': 10, 'k8805': 6, 'sorialgi': 80},
    'show' : function(){
        for(var name in this.list){
            document.write(name+':'+this.list[name]+"<br />");
        }
    }
};
grades.show();
```



