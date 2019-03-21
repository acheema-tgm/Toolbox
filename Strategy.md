## Strategy Pattern
### Beschreibung
Das Strategy Pattern ist ein **behavior-pattern**. Es ermöglicht es Algorithmen und 'behaivor' währen der laufzeit zu ändern.
Es definiert eine Familie von Algorithmen, kapselt sie einzeln und macht sie austauschbar.
Ganz nach dem Motto **Program to an interface, not an implementation.**

### Beispiel: Ente

Hier das BSP aus dem O'REILLY Buch 'Head First Design Patterns'  
[https://github.com/bethrobson/Head-First-Design-Patterns]
Context:
```java
public abstract class Duck {
	FlyBehavior flyBehavior;
	QuackBehavior quackBehavior;

	public Duck() {
	}

	public void setFlyBehavior(FlyBehavior fb) {
		flyBehavior = fb;
	}

	public void setQuackBehavior(QuackBehavior qb) {
		quackBehavior = qb;
	}

	abstract void display();

	public void performFly() {
		flyBehavior.fly();
	}

	public void performQuack() {
		quackBehavior.quack();
	}

	public void swim() {
		System.out.println("All ducks float, even decoys!");
	}
}
```
ConcreteContext:
```java
public class DecoyDuck extends Duck {
	public DecoyDuck() {
		setFlyBehavior(new FlyNoWay());
		setQuackBehavior(new MuteQuack());
	}
	public void display() {
		System.out.println("I'm a duck Decoy");
	}
}
```
Strategy(Interface):
```java
public interface QuackBehavior {
	public void quack();
}
```
ConcreteStrategy:
```java
public class FakeQuack implements QuackBehavior {
	public void quack() {
		System.out.println("Qwak");
	}
}
```
