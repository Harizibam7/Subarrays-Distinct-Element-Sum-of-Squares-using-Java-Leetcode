# Subarrays-Distinct-Element-Sum-of-Squares-using-Java-Leetcode

    class Solution {
        public int sumCounts(List<Integer> nums) {
            int n = nums.size();
            int ans = 0;
            for(int i =0; i<n;i++){
                HashSet<Integer> set = new HashSet<>();
                for(int j =i;j<n;j++){
                    set.add(nums.get(j));
                    ans += (set.size()*set.size());
                }
            }
            return ans;
        }
    }
