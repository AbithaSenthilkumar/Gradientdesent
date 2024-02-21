# Gradientdesent

#include <stdio.h>

// Changed function names to be more descriptive
void compute_gradient_wrt_w1(float x1, float x2, float y, float w1, float w2)
{
    // Computing gradient with respect to w1
    float gradient_w1 = 2 * (y - ((w1 * x1) + (w2 * x2))) * (-x1);
    printf("Gradient with respect to w1: %f\n", gradient_w1);
}

void compute_gradient_wrt_w2(float x1, float x2, float y, float w1, float w2)
{
    // Computing gradient with respect to w2
    float gradient_w2 = 2 * (y - ((w1 * x1) + (w2 * x2))) * (-x2);
    printf("Gradient with respect to w2: %f\n", gradient_w2);
}

int main() {
    // Changed data types of w1 and w2 to float
    float w1 = 1.0, w2 = 7.0;

    // Data array containing x1, x2, and y values
    float arr[4][3] = {{0, 1, 1}, {2, 1, 9}, {1, 0, 1}, {-2, 1, 7}};

    // Loop through each data point
    for (int i = 0; i < 4; i++) {
        // Compute gradients for each data point
        compute_gradient_wrt_w1(arr[i][0], arr[i][1], arr[i][2], w1, w2);
        compute_gradient_wrt_w2(arr[i][0], arr[i][1], arr[i][2], w1, w2);
    }
    return 0;
}
Explanation of C
