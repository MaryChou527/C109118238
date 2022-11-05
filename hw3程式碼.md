##### 請新增一個CShape的子類別CTriangle，其constructor共有三個double的參數 a,b,c (為直角三角形的三個邊長)，
##### 其面積為0.5ab，請寫出CTriangle的類別程式與產生其物件的main程式(顏色為紅色，a=3, b=4, c=5)程式碼請放在個人的github答案請列出其連結

```java

CShape.java        
abstract class CShape{
    protected String color;
    public void setColor(String str){
        color = str;
    }
 
    public abstract void show();
}

           
CTriangle.java
class CTriangle extends CShape{
    double ca, cb, cc;
    public CTriangle(double a, double b, double c){
        ca=a;
        cb=b;
        cc=c;
    }
   
    public void show() {
       
        System.out.print("color="+color+"  ");
        System.out.print("area="+0.5*ca*cb);
    }
   
}
app11.java
public class app11 {
   public static void main(String[] args) {
    CTriangle ct = new CTriangle(3, 4, 5);
    ct.setColor("red");
    ct.show();
}
}

```
