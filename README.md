    #include<stdio.h>

    int main(){
    float coefficients[2][3] = {0}; // 2D array to store a1, b1, c1, a2, b2, c2
    char* labels[3] = {"a", "b", "c"};
    char* labels[3] = {"a", "b", "c"};

    for(int i = 0; i < 2; i++){
        for(int j = 0; j < 3; j++){
            printf("Enter %s%d =\n", labels[j], i+1);
            scanf("%f", &coefficients[i][j]);
        }
    }

    printf("Given Eq. are:\n");
    for(int i = 0; i < 2; i++){
        printf("%fx + %fy = %f\n", coefficients[i][0], coefficients[i][1], coefficients[i][2]);
    }

    if (((coefficients[0][0]/coefficients[1][0]) == (coefficients[0][1]/coefficients[1][1])) && ((coefficients[0][1]/coefficients[1][1]) == (coefficients[0][2]/coefficients[1][2]))){ 
        printf("Lines are coincident, There are Infinite solutions for x and y");
    }
    else if (((coefficients[0][0]/coefficients[1][0]) == (coefficients[0][1]/coefficients[1][1])) && ((coefficients[0][1]/coefficients[1][1]) != (coefficients[0][2]/coefficients[1][2]))){
        printf("Lines are parallel, There are no solutions for x and y");
    }
    else{
        printf("Lines intersect at a point, There is a unique solution for x and y");
    }

    return 0;
}
