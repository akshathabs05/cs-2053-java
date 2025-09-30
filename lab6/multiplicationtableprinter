package lab6;

public class multiplicationprinter {
    
    public synchronized void printTable(int number) {
        for (int i = 1; i <= 10; i++) {
            System.out.println(number + " x " + i + " = " + (number * i));
            try {
                Thread.sleep(100); 
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

    public static void main(String[] args) {
     multiplicationprinter table = new multiplicationprinter();

        Thread t1 = new Thread(() -> {
            table.printTable(5);
        }, "Thread-1");

        Thread t2 = new Thread(() -> {
            table.printTable(5);
        }, "Thread-2");

        t1.start();
        t2.start();
    }
}
