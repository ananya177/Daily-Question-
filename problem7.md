#leetcode
#problem: Search a 2D matrix
#Solution
#Coding C++
#Done by ananya agarwal
#Easy approach :binary search algorithm
bool searchMatrix(vector<vector<int>>& matrix, int target) {
       
         if(matrix.empty() || matrix.size()==0 || matrix[0].size()==0) 
            return false;
        int r=matrix.size();
        int c=matrix[0].size();
        //binary search algorithm
        int start;
        int end;
        for(int i=0;i<r;i++)
        {     
            start=0;
            end=c-1;
         
        while(start<=end)
        {
            int middle=(start+end)/2;
           
            if(matrix[i][middle]==target)
                return true;
            if(matrix[i][middle]<target)
                start=middle+1;
            else
                end=middle-1;
        }
        }
        return false;
      
    }
    #Thank You
