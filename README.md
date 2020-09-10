# Triangle-class-java
Triangle
public class GeometricObject {
    private String color = "Red";
    private boolean filled;
    public GeometricObject(String color, boolean filled){
        this.color = color;
        this.filled = filled;
        
    }
    public String getColor(){
        return color;
    }
    public void setColor(String color){
        this.color = color;
    }
    public boolean isFilled(){
        return filled;
    }
    public void setFilled(boolean filled){
        this.filled = filled;
    }
        
    public String toString(){
        return "color: " + color + "and filled:" + filled;
    }
}



public class Triangle extends GeometricObject{
    private double length;
    private double breadth;
    private double height;
}
public Triangle(){
    
}
public Triangle(double length, double breadth, double height){
    this.length = length;
    this.breadth = breadth;
    this.height = height;
}
public Triangle(double length, double breadth,double height, String color , boolean filled){
    this.length = length;
    this.breadth = breadth;
    this.height = height;
    setColor(color);
    setFilled(filled);
}
public double getLength(){
    return length;
}
public void setLength(double length) {
    this.length = length;
}
public double getBreadth(){
   return breadth;
}
public void setBreadth (double breadth ){
    this.breadth = breadth;
}
public double getHeight(){
    return height;
}
public void setHeight(double height) {
    this.height= height;
}
public double getArea(){
    return 0.5 * length * breadth * height;
}
public double getPerimeter(){
    retrun length + breadth + height;
}


public class Tri{
    public static void main (String[] args){
        Triangle triangle = new Triangle(1, 2, 3);
        System.out.println("Triangle : " + triangle.toString());
        System.out.println ("Area of Triangle is: " + triangle.getArea());
        System.out.println("Perimeter of Trianlge is: " + triangle.getPerimeter());
    }
}
