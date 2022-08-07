# 
package B;

class penentu {
    public double hari;
    public double bulan;
    public double tahun;
    public double has;
    public double  i;
    public String ahir="Y";
   
    private double hastgl,k,t,f,kk;

   

   
    public double getHastgl() {
        return hastgl=tahun+bulan/12+hari/365;
    }

   
    public void setHastgl(double hastgl) {
        this.hastgl = hastgl;
    }

    
    public double getK() {
        return k=(hastgl-2000)*12.3685;
    }

   
    public void setK(double k) {
        this.k = k;
    }
     public double getKk() {
        return kk=(int)k+0.5;
    }

  
    public void setKk(double kk) {
        this.kk = kk;
    }


    
    public double getT() {
        return t= kk/1236.85;
    }

   
    public void setT(double t) {
        this.t = t;
    }

   
    public double getF() {
        return f=(160.7108+390.67050274*kk-0.0016431*t*t)%360;
    }

   
    public void setF(double f) {
        this.f = f;
    }

  
   
   
}
package B;

import javax.swing.JOptionPane;
public class gerhana {
  
    public static void main(String[] args) {
        
        
      
        penentu gerhana=new penentu();
        
        gerhana.i=Double.parseDouble(JOptionPane.showInputDialog(null,"==================== MENU =========================="+"\n1.menghitungg"+"\n2.keluar"));
        if(gerhana.i==1){
        gerhana.hari=Double.parseDouble(JOptionPane.showInputDialog(null,"masukan tanggal hari : "));
        gerhana.bulan=Double.parseDouble(JOptionPane.showInputDialog(null,"masukan tanggal bulan : "));
      gerhana.tahun=Double.parseDouble(JOptionPane.showInputDialog(null,"masukan tanggal tahun : "));
     
    if(gerhana.getF()-180>21){JOptionPane.showInternalMessageDialog(null,"terjadi");}
    else if (gerhana.getF()-180<13.9){JOptionPane.showInternalMessageDialog(null,"tidak");}
            try {gerhana.ahir=JOptionPane.showInputDialog(null,"apakah inggin melanjutkan Y/T");
                
            } catch (Exception e) {
            }
        }
        else{JOptionPane.showMessageDialog(null,"terimakasih");}
        gerhana.i++;
}
 
}

