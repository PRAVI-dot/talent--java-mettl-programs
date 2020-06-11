# talent--java-mettl-programs
class Result { public static int find(char[] a, char target) { int i; for (i = 0; i < 9; i++) if (a[i] == target) break; return i; }

public static int entryTime(String s, String keypad) { char[] keyboard = keypad.toCharArray(); char[] str = s.toCharArray(); int index = find(keyboard,str[0]); int pos_i,pos_j; pos_i = index/3; pos_j = index%3; int curr_index,curr_i,curr_j; int time=0,curr; for(int i=1;i < str.length; i++){ curr_index = find(keyboard,str[i]); curr_i = curr_index/3; curr_j = curr_index%3; //System.out.println(curr_i+" "+curr_j); curr = Math.max(Math.abs(pos_i-curr_i),Math.abs(pos_j-curr_j)); time = time + curr; pos_i = curr_i; pos_j = curr_j;

} return time;

}

}
