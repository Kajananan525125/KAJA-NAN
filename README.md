public class Mobile
{
    void iphone(){
        System.out.println("This is iphone");
    }
    void samsung(){
        System.out.println("This is Samsung phone");
    }

    public static void main(String[] args) {
        Mobile obj1=new Mobile();
        obj1.iphone();
        Mobile obj2=new Mobile();
        obj2.samsung();
    }
}
