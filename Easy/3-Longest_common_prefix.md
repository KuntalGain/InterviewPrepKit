```
class Solution {
public:
    string longestCommonPrefix(vector<string>& s) {
        
        int ans = s[0].length();      //length of the string
        int n = s.size();             //length of the string array
        
      //traverse the every string elemnet
        for(int i = 1 ; i < n ; i++){
            int j = 0;
            
            while(j < s[i].length() && s[i][j] == s[0][j])
                j++;            //update j
            
            ans = min (ans , j);
        }
        
        return s[0].substr(0,ans);
    }
};
``` 
