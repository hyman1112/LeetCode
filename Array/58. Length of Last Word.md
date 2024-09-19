## 想法
第一個for迴圈是從尾巴開始搜尋陣列，然後找到第一個不是空格的字元的位址。

第二個for迴圈就從那個位址開始算這個字詞的長度然後最輸出。

```CPP
class Solution {
public:
    int lengthOfLastWord(string s) {
        int count = 0;
        int index;
        for(int i = s.length() - 1 ; i >= 0 ; i--)
        {
            if(s[i] != ' ')
            {
                index = i;
                break;
            }
        }

        for(int i = index ; i >= 0 ; i--)
        {
            if(s[i] != ' ')
            {
                count++;
            }
            else
            {
                break;
            }
        }
        return count;
    }
};
```
