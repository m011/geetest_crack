# geetest_crack 2*3.0.0
geetest 2*3.0.0 version crack       
Focus on line 6132 and following code does some magic.      
```{java}
private String new_func(String str) {
        String m;
        int n = 0;
        String ss = str;
        int c0 = Integer.parseInt(this.cList[0]);
        int c2 = Integer.parseInt(this.cList[2]);
        int c4 = Integer.parseInt(this.cList[4]);
        for (int i = 0; i < 4; i++) {
            m = this.sString.substring(n, n + 2);
            n += 2;
            int k = Integer.parseInt(m, 16);
            String v = fromCharCode(k);
            int q = (c0 * k * k + c2 * k + c4) % str.length();
            ss = ss.substring(0, q) + v + ss.substring(q);
        }
        return ss;
    }
```
