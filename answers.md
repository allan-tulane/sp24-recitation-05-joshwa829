# CMPS 2200 Reciation 5
## Answers

**Name:**_____Joshua Allison ____________________


Place all written answers from `recitation-05.md` here for easier grading.







- **1b.**
Quicksort with a Fixed Pivot exhibits challenges when sorting pre-sorted lists, showcasing its worst-case O(n^2) behavior. However, it demonstrates improved performance on shuffled lists, achieving closer to the expected average-case O(nlog⁡n) efficiency.
Quicksort with a Random Pivot maintains consistent performance across both sorted and shuffled lists, aligning with its expected O(nlogn) time complexity. Notably, it outperforms the fixed-pivot variant when sorting pre-sorted lists.
TimSort excels in all scenarios, showcasing superior efficiency, particularly on pre-sorted lists where its performance is optimal. With best-case efficiency approaching 
O(n) and generally operating at 
O(nlogn), TimSort demonstrates robust performance across different list types.

Comparing on sorted lists:

|   List Size |   QSort-Fixed-Pivot (ms) |   QSort-Random-Pivot (ms) |   TimSort (ms) |
|-------------|--------------------------|---------------------------|----------------|
|          50 |                    0.286 |                                 0.083 |          0.001 |
|         100 |                    0.799 |                                 0.167 |          0.001 |
|         150 |                    1.854 |                                 0.248 |          0.002 |
|         200 |                    3.091 |                                 0.333 |          0.001 |
|         250 |                    5.045 |                                 0.386 |          0.002 |
|         300 |                    7.451 |                                 0.482 |          0.003 |
|         350 |                    9.991 |                                 0.533 |          0.003 |
|         400 |                   13.715 |                                 0.621 |          0.002 |
|         450 |                   16.673 |                                 0.690 |          0.002 |
|         500 |                   20.320 |                                 0.799 |          0.003 |



Comparing on shuffled lists:

|   List Size |   QSort-Fixed-Pivot (ms) |   QSort-Random-Pivot (ms) |   TimSort (ms) |
|-------------|--------------------------|---------------------------|----------------|
|          50 |                    0.067 |                                 0.065 |              0.004 |
|         100 |                    0.121 |                                  0.129 |          0.007 |
|         150 |                    0.197 |                                  0.207 |          0.009 |
|         200 |                    0.285 |                                  0.298 |          0.013 |
|         250 |                    0.335 |                                  0.417 |          0.016 |
|         300 |                    0.451 |                                  0.450 |          0.019 |
|         350 |                    0.472 |                                  0.525 |          0.022 |
|         400 |                    0.555 |                                  0.611 |          0.026 |
|         450 |                    0.659 |                                  0.719 |          0.030 |
|         500 |                    0.735 |                                  0.889 |          0.034 |






- **1c.**
When comparing the faster variant of Quicksort, which uses a random pivot, to Python's sorted function, which implements TimSort, several considerations emerge:
In scenarios involving shuffled lists, both algorithms target achieving an efficiency of O(nlogn). However, due to TimSort's implementation optimizations, it's expected to surpass Quicksort's performance in most cases.
On lists that are already sorted, TimSort's design, tailored to exploit existing order, significantly outperforms Quicksort. This is primarily due to TimSort's ability to recognize and efficiently handle pre-sorted sequences, resulting in enhanced performance compared to Quicksort's approach.