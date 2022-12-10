# ticketprice
    import java.util.Scanner;

    public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int km, yas,x;
        double tutar, yasIndirimi, indirimliTutar, gd;
        System.out.print("Mesafeyi km türünden giriniz: ");
        km= input.nextInt();
        if(km<0){
            System.out.println("Hatalı mesafe girişi, tekrar deneyin.");
            return;
        }
        System.out.print("Yaşınızı giriniz: ");
        yas= input.nextInt();
        tutar= km*0.10;
        System.out.println("Tutar: " +tutar);
        if(yas<0){
            System.out.println("Hatalı yaş girişi, tekrar deneyin.");
            return;
        }
        if(yas<12){
            System.out.print("Gidiş dönüş =>1 , Tek yön =>2\nSeçiniz:   ");
            x= input.nextInt();
            if(x==1){
                yasIndirimi= tutar*0.5;
                indirimliTutar= tutar - yasIndirimi;
                gd= indirimliTutar* 0.2;
                System.out.println("İndirimli tutar: " + gd*2);

            }else{
                yasIndirimi= tutar*0.5;
                indirimliTutar= tutar - yasIndirimi;
                System.out.println("İndirimli tutar: " + indirimliTutar);
            }
        }
        else if((yas>=12) && (yas<=24) ){
            System.out.print("Gidiş dönüş =>1 , Tek yön =>2\nSeçiniz:   ");
            x= input.nextInt();
            if(x<0){
                System.out.println("Hatalı seçim, tekrar deneyin.");
            }
            if(x==1){
                yasIndirimi= tutar*0.1;
                indirimliTutar= tutar - yasIndirimi;
                gd= indirimliTutar* 0.2;
                System.out.println("İndirimli tutar: " + gd*2);

            }else{
                yasIndirimi= tutar*0.1;
                indirimliTutar= tutar - yasIndirimi;
                System.out.println("İndirimli tutar: " + indirimliTutar);
            }
        }
        else if((yas>24) && (yas<=65)){
            System.out.println("Herhangi bir indirim uygulanamıyor. ");
        }
        else{
            System.out.print("Gidiş dönüş =>1 , Tek yön =>2\nSeçiniz:   ");
            x= input.nextInt();
            if(x<0){
                System.out.println("Hatalı seçim, tekrar deneyin.");
            }
            if(x==1){
                yasIndirimi= tutar*0.3;
                indirimliTutar= tutar - yasIndirimi;
                gd= indirimliTutar* 0.2;
                System.out.println("İndirimli tutar: " + gd*2);

            }else{
                yasIndirimi= tutar*0.3;
                indirimliTutar= tutar - yasIndirimi;
                System.out.println("İndirimli tutar: " + indirimliTutar);
            }
        }
    }
}
