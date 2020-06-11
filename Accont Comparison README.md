# talent--java-mettl-programs
class Account implements OnlineAccount, Comparable {

int noOfRegularMovies, noOfExclusiveMovies; String ownerName;

// 1) Add a parameterized constructor that initializes the attributes noOfRegularMovies and noOfExclusiveMovies. Account (String oname,int nrm, int nem) { this.ownerName = oname; this.noOfRegularMovies=nrm; this.noOfExclusiveMovies=nem; }

// 2. This method returns the monthly cost for the account. public int monthlyCost() { return basePrice + (noOfRegularMoviesregularMoviePrice) + (noOfExclusiveMoviesexclusiveMoviePrice); }

// 3. Override the compareTo method of the Comparable interface such that two accounts can be compared based on their monthly cost. @Override public int compareTo(Account o) { // TODO Auto-generated method stub if (this.monthlyCost()>o.monthlyCost()) { this.toString(); return 1; } else { o.toString (); return -1; }

}

// 4. Returns "Owner is [ownerName] and monthly cost is [monthlyCost] USD." public String toString() { String s = new String (); s="Owner is " + ownerName + " and monthly cost is " + monthlyCost() + " USD."; return s;

} }
