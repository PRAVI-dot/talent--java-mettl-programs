# talent--java-mettl-programs
class Result {

/*

Complete the 'smallestString' function below.
The function is expected to return a STRING.
The function accepts STRING_ARRAY substrings as parameter. */ static void sort(String a[], int n) { for(int i = 0;i < n;i++) { for(int j = i + 1;j < n;j++) { if((a[i] + a[j]).compareTo(a[j] + a[i]) > 0) { String s = a[i]; a[i] = a[j]; a[j] = s; } } } }
public static String smallestString(List substrings) { // Write your code here String str[] = new String[substrings.size()]; for (int j = 0; j < substrings.size(); j++) { str[j] = substrings.get(j); } int n=str.length; sort(str,n); String answer = ""; for (int i = 0; i < n; i++) answer += str[i]; return answer;

}

}

Announcement: "Virtusa Test-4 - Keyboard - Solution…" Maria Michael Visuwasam L Created May 30May 30 Virtusa Test-4 - Keyboard - Solution

class Result {

/*
Complete the 'entryTime' function below.
The function is expected to return an INTEGER.
The function accepts following parameters:
STRING s
STRING keypad */
public static int find(char[] a, char target) { int i; for (i = 0; i < 9; i++) if (a[i] == target) break; return i; }

public static int entryTime(String s, String keypad) { char[] keyboard = keypad.toCharArray(); char[] str = s.toCharArray(); int index = find(keyboard,str[0]); int pos_i,pos_j; pos_i = index/3; pos_j = index%3; int curr_index,curr_i,curr_j; int time=0,curr; for(int
i=1;i < str.length; i++){ curr_index = find(keyboard,str[i]); curr_i = curr_index/3; curr_j = curr_index%3; //System.out.println(curr_i+" "+curr_j); curr = Math.max(Math.abs(pos_i-curr_i),Math.abs(pos_j-curr_j)); time = time + curr; pos_i = curr_i; pos_j = curr_j;

} return time;

}

}
