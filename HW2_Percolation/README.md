HW Requirements: https://hackmd.io/@CiqLOooyRwWmK--mMkfetA/Bya-c-feo  <br />
Textbook: https://coursera.cs.princeton.edu/algs4/assignments/percolation/specification.php

Union-Find object ```PointsUF``` to check if the Point ```isFull(int i, int j)``` or if the system ```percolates() ```
```java
 WeightedQuickUnionUF PointsUF;
```
```PercoPoints``` store the Points(in Point2D) in Percolated Region at the moment percolation just happened

```java
if(!RECORDED){
         if(percolates()){
            for(int id : OpenPoints_id){
               if(PointsUF.find(id)==PointsUF.find(top_id)){
                  int x = (id-1)/size;
                  int y = (id-1)%size;
                  Point2D point = new Point2D(x, y);
                  PercoPoints.add(point);
                  RECORDED = true;
               }
            }
         }
      }
```
<br />
Notice: the Percolated Region does not include the backwash Points
