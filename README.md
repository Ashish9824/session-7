# session-7

### Task 1: 5x5 Instagram Post Feed Grid

```c
#include <stdio.h>

int main() {
    int rows = 5;
    int cols = 5;

    // Outer loop controls rows
    for (int i = 0; i < rows; i++) {
        // Inner loop controls columns
        for (int j = 0; j < cols; j++) {
            printf("[📷] ");
        }
        printf("\n"); // Move to next row
    }

    return 0;
}

```

**Output:**

```text
[📷] [📷] [📷] [📷] [📷] 
[📷] [📷] [📷] [📷] [📷] 
[📷] [📷] [📷] [📷] [📷] 
[📷] [📷] [📷] [📷] [📷] 
[📷] [📷] [📷] [📷] [📷] 

```

---

### Task 2: Right-Angled Number Triangle (Leaderboard Ranks)

```c
#include <stdio.h>

int main() {
    int n = 5; // Height of leaderboard triangle

    for (int i = 1; i <= n; i++) {
        // Print ranks starting from 1 up to current row number
        for (int j = 1; j <= i; j++) {
            printf("%d ", j);
        }
        printf("\n");
    }

    return 0;
}

```

**Output:**

```text
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5 

```

---

### Task 3: 6-Row Centered Star Pyramid

For each row `i` (from 1 to `rows`):

* Leading spaces: `rows - i`
* Stars printed: `2 * i - 1`

```c
#include <stdio.h>

int main() {
    int rows = 6;

    for (int i = 1; i <= rows; i++) {
        // Inner loop 1: Print leading alignment spaces
        for (int space = 1; space <= rows - i; space++) {
            printf(" ");
        }

        // Inner loop 2: Print odd number of stars (2*i - 1)
        for (int star = 1; star <= (2 * i - 1); star++) {
            printf("*");
        }

        printf("\n");
    }

    return 0;
}

```

**Output:**

```text
     *
    ***
   *****
  *******
 *********
***********

```

---

### Task 4: Alternating 0s and 1s Checkered Grid (4x4)

Alternating cells can be determined by checking whether the sum of coordinates `(row + col)` is even or odd:

```c
#include <stdio.h>

int main() {
    int size = 4; // 4x4 grid

    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            // If the sum of row and col indices is even, print 1; else 0
            if ((i + j) % 2 == 0) {
                printf("1 ");
            } else {
                printf("0 ");
            }
        }
        printf("\n");
    }

    return 0;
}

```

**Output:**

```text
1 0 1 0 
0 1 0 1 
1 0 1 0 
0 1 0 1 

```

---

### Task 5: User-Input Pyramid Height

```c
#include <stdio.h>

int main() {
    int rows;

    printf("Enter the height of the pyramid (number of rows): ");
    scanf("%d", &rows);

    if (rows <= 0) {
        printf("Please enter a positive integer greater than 0.\n");
        return 1;
    }

    for (int i = 1; i <= rows; i++) {
        // Print leading spaces
        for (int space = 1; space <= rows - i; space++) {
            printf(" ");
        }

        // Print stars
        for (int star = 1; star <= (2 * i - 1); star++) {
            printf("*");
        }

        printf("\n");
    }

    return 0;
}

```
