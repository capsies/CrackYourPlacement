//solution using hash map - O(N) complexity
//count() - used to find if a key is present in a hashmap or not in C++

class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int k) {
        unordered_map<int,int> mp;
        for(int i=0;i<nums.size();i++){
            if(mp.count(k-nums[i]))return {mp[k-nums[i]],i};
            mp[nums[i]]=i;
        }
        return {-1,-1};
    }
};
