#leetcode
#Solution
#Climbing Stairs
#Coding C++
#Done bu Ananya Agarwal
    int climbStairs(int n) {
        
        int dp[n+1];//Number of ways we can climb
        if(n==1)
            return 1;
        if(n==2)
            return 2;
        
        dp[1]=1;//1 stairs case 1 way to climb
        dp[2]=2;//2stairs cases 2 ways to climb  1step+1step=1 way and 2step=2ways
        //for other cases
        for(int i=3;i<=n;i++)
            dp[i]=dp[i-1]+dp[i-2];
        return dp[n];
 }
 #Thank you
