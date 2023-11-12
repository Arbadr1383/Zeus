using System;

class Program
{
    static void Main()
    {
        // تعریف متغیرها
        int numberOfAccounts;
        double totalBalance = 0;

        // دریافت تعداد حساب‌ها از کاربر
        Console.Write("تعداد حساب‌ها: ");
        while (!int.TryParse(Console.ReadLine(), out numberOfAccounts) || numberOfAccounts <= 0)
        {
            Console.Write("لطفاً یک عدد صحیح و مثبت وارد کنید: ");
        }

        // دریافت موجودی هر حساب و محاسبه کل موجودی
        for (int i = 1; i <= numberOfAccounts; i++)
        {
            Console.Write($"موجودی حساب {i}: ");
            while (!double.TryParse(Console.ReadLine(), out double accountBalance) || accountBalance < 0)
            {
                Console.Write("لطفاً یک عدد مثبت وارد کنید: ");
            }

            totalBalance += accountBalance;
        }

        // نمایش کل موجودی حساب‌ها
        Console.WriteLine($"کل موجودی حساب‌ها: {totalBalance}");

        // منتظر نگه داشتن نتیجه تا فشار دادن یک دکمه توسط کاربر
        Console.ReadLine();
    }
}