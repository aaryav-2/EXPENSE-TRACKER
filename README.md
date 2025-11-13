# EXPENSE-TRACKER

    #include <stdio.h>

    float sumExpenses(float *expenses, int n)
    {
   
    if (n == 0)
        return 0;
    
    return expenses[n - 1] + sumExpenses(expenses, n - 1);
        }

        void main() 
         {
    int n;
    float total = 0;

    printf("Enter the number of expenses for the month: ");
    scanf("%d", &n);

    float expenses[n];  

    printf("\nEnter the amount for each expense:\n");
    for (int i = 1; i<=n; i++) {
        printf("Expense %d: ", i );
        scanf("%f", &expenses[i]);
    }

    total = sumExpenses(expenses, n);

    printf("\nTotal monthly expenses = %.2f\n", total);

     }
