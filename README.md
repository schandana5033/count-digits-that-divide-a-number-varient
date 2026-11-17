# count-digits-that-divide-a-number-varient
class Solution {
    public int countDigits(int num) {
        int value = num, count = 0;
        while (value > 0) {
            int digit = value % 10;
            if (digit != 0 && num % digit == 0) count++;
            value /= 10;
        }
        return count;
    }
}
// Time: O(log10 n) | Space: O(1)
