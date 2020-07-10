#leetcode
#Problem:Spiral martix
#Solution
#Coding C++
#Done by Ananya Agarwal
 vector<int> spiralOrder(vector<vector<int>>& matrix) {
    vector<int> M;
    int r=matrix.size();
    if(matrix.size()==0)
         return M;
     int c=matrix[0].size();
      
     int r1=0;
     int c1=0;
 
     while(r1<r && c1<c)
     {
            for(int i=c1;i<c;i++)
                M.push_back(matrix[r1][i]);
            r1++;
            for(int i=r1;i<r;i++)
                M.push_back(matrix[i][c-1]);
            c--;
            if(r1<r)
            {
                for(int i=c-1;i>=c1;i--)
                    M.push_back(matrix[r-1][i]);
                r--;
                
            }
         if(c1<c)
         {
             for(int i=r-1;i>=r1;i--)
                 M.push_back(matrix[i][c1]);
             c1++;
         }
        
     }
       return M;  
   
    }
    
    #Thank You
