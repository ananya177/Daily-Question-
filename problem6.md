#Leetcode
#Lucky NUmber
#Solution
#Coding C++
#Done by Ananya Agarwal
#Approach is easy
#1-Need to find the min of rows views
#2-Need to find the maximum element colunm views
#3-Check which is common element thats is the Lucky number

 vector<int> luckyNumbers (vector<vector<int>>& matrix) {
        vector<int> V,C;
        int min;
        for(int i=0;i<matrix.size();i++)
        {
            min=INT_MAX;
            for(int j=0;j<matrix[0].size();j++)
            {
                if(min>matrix[i][j])
                {
                    min=matrix[i][j];
                   
                }
                 
            }
             V.push_back(min);
        }
        int max;
        for(int i=0;i<matrix[0].size();i++)
        {
            max=INT_MIN;
            for(int j=0;j<matrix.size();j++)
            {
                if(max<matrix[j][i])
                {
                    max=matrix[j][i];
                   
                }
                 
            }
             C.push_back(max);
        }
        vector<int> result;
        for(int i=0;i<V.size();i++)
        {
            for(int j=0;j<C.size();j++)
            {
                if(V[i]==C[j])
                    result.push_back(V[i]);
            }
        }
        return result;
      
    }

