#LeetCode 
#Solution
#Valid Parentheses
#Done By Ananya Agarwal
#Coding C++
 bool isValid(string s) {
        
        stack<char> S;
        for(int i=0;i<s.length();i++)
        {
            char c=s[i];
            switch(c)
            {
                case '(':
                case '[':
                case '{':
                    S.push(c);
                    break;
                case ')':
                    if(!S.empty())
                    {
                        if(S.top()=='(')
                            S.pop();
                        else
                            return false;
                        
                    }
                    else
                        return false;
                   break;
                case ']':
                   if(!S.empty())
                    {
                        if(S.top()=='[')
                            S.pop();
                        else
                            return false;
                        
                    }
                    else
                        return false;
                   break;
                case '}':
                    if(!S.empty())
                    {
                        if(S.top()=='{')
                            S.pop();
                        else
                            return false;
                        
                    }
                    else
                        return false;
                   break;
                        
            }
            
        }
        
        return S.empty();
 }
 # THank you
