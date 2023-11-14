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

_________________________________________________


import android.app.AlarmManager
import android.app.PendingIntent
import android.content.BroadcastReceiver
import android.content.Context
import android.content.Intent
import java.util.*

class SchedulerReceiver : BroadcastReceiver() {
    override fun onReceive(context: Context?, intent: Intent?) {
        // اجرای کد مرتبط با زمان بندی اینجا
    }
}

class MyScheduler {
    fun scheduleTask(context: Context?, hour: Int, minute: Int) {
        val alarmManager = context?.getSystemService(Context.ALARM_SERVICE) as AlarmManager
        val intent = Intent(context, SchedulerReceiver::class.java)
        val pendingIntent = PendingIntent.getBroadcast(context, 0, intent, 0)

        // تنظیم زمان بندی
        val calendar = Calendar.getInstance()
        calendar.set(Calendar.HOUR_OF_DAY, hour)
        calendar.set(Calendar.MINUTE, minute)
        calendar.set(Calendar.SECOND, 0)

        // تعریف نوع تکرار (در اینجا یکبار در روز)
        alarmManager.setRepeating(
            AlarmManager.RTC_WAKEUP,
            calendar.timeInMillis,
            AlarmManager.INTERVAL_
}




_______________________________________________