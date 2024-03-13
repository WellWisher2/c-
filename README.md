```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
namespace lab_program_10 {
class Shape {
  public virtual void draw() { Console.WriteLine("Drawing a shape"); }
  public virtual void erase() { Console.WriteLine("Erasing a shape"); }
}
class Circle : Shape {
  public override void draw() { Console.WriteLine("Drawing a circle"); }
  public override void erase() { Console.WriteLine("Erasing a circle"); }
}
class Triangle : Shape {
  public override void draw() { Console.WriteLine("Drawing a triangle"); }
  public override void erase() { Console.WriteLine("Erasing a triangle"); }
}
class Square : Shape {
  public override void draw() { Console.WriteLine("Drawing a square"); }
  public override void erase() { Console.WriteLine("Erasing a square"); }
}
class Program {
  static void Main(string[] args) {
    Shape[] shapes = new Shape[3];
    shapes[0] = new Circle();
    shapes[1] = new Triangle();
    shapes[2] = new Square();
    foreach (Shape shape in shapes) {
      shape.draw();
      shape.erase();
    }
    Console.ReadKey();
  }
}
}
```
