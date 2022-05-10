# leetcode

### 1859. Sorting the Sentence

<details>
  


Example 1:

Input: s = "is2 sentence4 This1 a3"
Output: "This is a sentence"
Explanation: Sort the words in s to their original positions "This1 is2 a3 sentence4", then remove the numbers.
  
  <summary>Code</summary>
  
  ```

  class Solution {
  public:
    string sortSentence(string s)
    {
        
    map<int,string>m;
        string st=" ";
        for(char c:s)
        {
            if(c<='9' && c>'0')
            {
                m[c-'0']=st;
                st.clear();continue;
            }
            st+=c;
        }
        string str;
        for(auto x:m)
            str+=x.second;
        return str.substr(1);
        
    }
   };
  
```
</details>
