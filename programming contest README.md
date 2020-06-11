# talent--java-mettl-programs
class Result {

public static int minimizeBias(List ratings) { // Write your code here int sum=0; int len = ratings.size(); Collections.sort(ratings); for(int i=0; i<len-1; i+=2){ int diff = ratings.get(i+1)-ratings.get(i); sum+= diff; } return sum; } }
