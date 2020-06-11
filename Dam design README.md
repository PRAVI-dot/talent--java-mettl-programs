# talent--java-mettl-programs
class Result { public static int maxHeight(List wallPositions, List wallHeights) { // Write your code here int l=0; for (int i=0; i<wallPositions.size()-1; i++) { if (wallPositions.get(i)<wallPositions.get(i+1)-1) { int height = Math.abs(wallHeights.get(i+1) - wallHeights.get(i)); int gap = wallPositions.get(i+1) - wallPositions.get(i) - 1; int localMax = 0; if (gap > height) { int low = Math.max(wallHeights.get(i+1), wallHeights.get(i)) + 1; int remainingGap = gap - height - 1; localMax = low + remainingGap/2;

} else { localMax = Math.min(wallHeights.get(i+1), wallHeights.get(i)) + gap; }

l= Math.max(l, localMax); } }

return l;

}

}
