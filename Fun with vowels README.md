# talent--java-mettl-programs
class Result { public static int longestVowelSubsequence(String s) { // Write your code here if (s.length() <= 0) throw new IllegalArgumentException();

Map<Character, Character> precCharMap = new HashMap<>(); precCharMap.put('u', 'o'); precCharMap.put('o', 'i'); precCharMap.put('i', 'e'); precCharMap.put('e', 'a');

Map<Character, String> runningLongestSubMap = new HashMap<>();

for (char currChar : s.toCharArray()) { String currCharLongestSub; String precCharLongestSub = null; if (currChar == 'a') { currCharLongestSub = runningLongestSubMap.getOrDefault(currChar, ""); } else { currCharLongestSub = runningLongestSubMap.get(currChar); char precChar = precCharMap.get(currChar); precCharLongestSub = runningLongestSubMap.get(precChar); } if (precCharLongestSub == null && currCharLongestSub != null) { updateRunningLongestSubMap(currCharLongestSub, currChar, runningLongestSubMap); } else if (currCharLongestSub == null && precCharLongestSub != null) { updateRunningLongestSubMap(precCharLongestSub, currChar, runningLongestSubMap); } else if (currCharLongestSub != null && precCharLongestSub != null) { if (currCharLongestSub.length() < precCharLongestSub.length()) { updateRunningLongestSubMap(precCharLongestSub, currChar, runningLongestSubMap); } else { updateRunningLongestSubMap(currCharLongestSub, currChar, runningLongestSubMap); } } }

if (runningLongestSubMap.get('u') == null) { return 0; } return runningLongestSubMap.get('u').length();

}

private static void updateRunningLongestSubMap(String longestSub, char currChar, Map<Character, String> runningLongestSubMap) { String currCharLongestSub = longestSub + currChar; runningLongestSubMap.put(currChar, currCharLongestSub); }

}
