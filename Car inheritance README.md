# talent--java-mettl-programs
class WagonR extends Car { int mil; public WagonR (int n) { super(false, "4"); this.mil=n;

} public String getMileage () { String s = new String (); s= mil + " kmpl"; return s; }

}

class HondaCity extends Car { int mil; public HondaCity (int n) { super(true, "4"); mil=n; } public String getMileage () { String s = new String (); s= mil + " kmpl"; return s; } } /**

InnovaCrysta class **/ class InnovaCrysta extends Car { int mil; public InnovaCrysta (int n) { super(false,"6"); mil=n; } public String getMileage () { String s = new String (); s= mil + " kmpl"; return s; }
}
