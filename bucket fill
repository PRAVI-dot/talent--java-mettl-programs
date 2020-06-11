class Result { static void floodFillUtil(char screen[][], int x, int y, int prevC,int M,int N) { if (x < 0 || x >= M || y < 0 || y >= N) return; if (screen[x][y] != prevC) return;

screen[x][y] = '-';

floodFillUtil(screen, x+1, y, prevC,M,N); floodFillUtil(screen, x-1, y, prevC,M,N); floodFillUtil(screen, x, y+1, prevC,M,N); floodFillUtil(screen, x, y-1, prevC,M,N); }

public static int strokesRequired(List picture) { // Write your code here char[][] screen=new char[10000][1000]; int i=0,count=0,x=0,y=0,m=0; for (String j:picture) { screen[i++]=j.toCharArray(); m=j.length(); }

for (int k=0;k<i;k++) { for (int p=0;p<m;p++) { if (screen[k][p]!='-') { count++; x=k; y=p; floodFillUtil(screen,x,y,screen[k][p],i,m); } } } return count;

}

}
