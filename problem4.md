#LeetCode 
#Soution 
#Majority Element
#Coding C++
#Done by Ananya Agarwal
#Easy Approach O(n) tc
int MajorityElement(Vector<int> &nums)
{
    int majorityElement(vector<int>& nums) {
        unordered_map<int,int> mp;
       
        for(auto i:nums)
        {
             mp[i]++;
            if(mp[i]>nums.size()/2)
                return i;
        }
        return -1;
        
        
    }

# O(N*N) tc
int majorityElement(vector<int>& nums) {
        int max=0;
        int index=-1;
        int n=nums.size();
        for(int i=0;i<nums.size();i++)
        {
            int count=0;
            for(int j=0;j<nums.size();j++)
            {
                if(nums[i]==nums[j])
                    count++;
                
            }
            if(count>max)
            {
                max=count;
                index=i;
            }
        }
       if(max>n/2)
           return nums[index];
        return -1;
        
    }
}
#thank you
