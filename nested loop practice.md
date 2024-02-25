  for(int i=1;i<=3;i++) {

for(int j=1;j<=3;j++) {

System.out.println(j); //Output: 123 123 123

}

}



1               2           3.1         3.2              3.3           3.4           4
i=1         1<=3      j=1        1<=3            j=1         j=2
                             j=2       2<=3            j=2         j=3
                             j=3       3<=3            j=3         j=4
                             j=4       4<=3  (inner loop terminated)  i=2
i=2         2<=3      j=1       1<=3            j=1          j=2 
                             j=2       2<=3            j=2          j=3
                             j=3       3<=3            j=3          j=4
                             j=4       4<=3(inner loop terminated)    i=3
i=3         3<=3      j=1       1<=3              j=1         j=2       
							j=2        2<=3              j=2         j=3
							j=3        3<=3              j=3         j=4
							j=4        4<=3  (Inner loop termainated) i=4
i=4         4<=3     (Outer loop canceled)



# 2 Excise:
                         1      2    4
    for (int i = 1; i <= 3; i++) {
                        3.1     3.2   3.4
      for (int j = 1; j <= 3; j++) {
         3.3 
        System.out.println(i);   //output :111  222  333

1             2            3.1       3.2         3.3         3.4                 4                                         
i=1       1<=3        j=1    1<=3         1            2
                            j=2     2<=3        1            3 
                            j=3     3<=3        1            4
                            j=4     4<=3 (inner loop terminated)    i=2
i=2        2<=3       j=1    1<=3        2             2
                             j=2    2<=3        2            3
                             j=3    3<=3        2            4
                             j=4     4<=3 (inner loop terminated)   i=3
i=3        3<=3       j=1     1<=3       3           2
                            j=2      2<=3      3            3
                            j=3      3<=3      3           4
                            j=4     4<=3   (Inner loop canceled)    i=4
i=4        4<=3    (Outer loop Canceled)                        


# 3 Excise
				       1       2     4
     for (int i = 1; i <= 3; i++) {
                      3.1      3.2   3.4
      for (int j = 1; j <= i; j++) {
                 3.3 
        System.out.println(j);
      }
1             2               3.1           3.2              3.3         3.4                4
i=1        1<=3         j=1           1<=1            1           2
                               j=2           2<=1(inner loop terminated)      i=2

i=2         2<=3        j=1            1<=2           1          2
                              j=2             2<=2           2          3 
                              j=3             3<=2 (inner loop terminated)    i=3

i=3         3<=3        j=1            1<=3          1           2
                              j=2             2<=3          2           3
                              j=3             3<=3          3           4
                              j=4             4<=3  (inner loop terminated)  i=4
i=4          4<=3 (Outer loop Terminated)

  