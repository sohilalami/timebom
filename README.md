# timebom

Mijn tijdbom samen gemaakt met Taurese

import java.util.Timer;
import java.util.TimerTask;

   public class Main {
     
      public static int beginTime = 6;
      public static void main(String[] args) {

        Timer timer = new Timer();
        timer.schedule(new TimerTask() {
            public void run() {
                if (beginTime == 0) {
                   System.out.println("YOU LOSE");
                   timer.cancel();
                   System.out.println("BOOOOMMM!!!");
                } else {
                   beginTime--;
                   System.out.println(beginTime);
                }
            }
        }, 0, 500);
    }
}
