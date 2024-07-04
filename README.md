Description of the script.js section

توضیحات بخش script.js

 1-The first part document.addEventListener("DOMContentLoaded", () => { ... });:

 This line of code ensures that all JavaScript code is executed only after the HTML content is fully loaded. This is done using a DOMContentLoaded event, which is called when all HTML content has been loaded and the DOM tree is complete.

1- توضیحات بخش اول document.addEventListener("DOMContentLoaded", () => { ... });:
این خط کد اطمینان حاصل می‌کند که تمامی کدهای جاوااسکریپت فقط پس از بارگذاری کامل محتوای HTML اجرا شوند. این کار با استفاده از یک رویداد DOMContentLoaded انجام می‌شود که وقتی تمام محتوای HTML بارگذاری شده و درخت DOM کامل شده است، فراخوانی می‌شود.

2-The second part contains const totalSeconds = 21 * 3600 + 46 * 60 + 45;:

In this line, the total number of seconds the timer should run is calculated. Here, the timer is set for 21 hours, 46 minutes and 45 seconds. This value is converted to seconds for ease of use in code.

2- توضیحات بخش دوم const totalSeconds = 21 * 3600 + 46 * 60 + 45;:

در این خط، تعداد کل ثانیه‌هایی که تایمر باید اجرا شود محاسبه می‌شود. در اینجا، تایمر برای 21 ساعت، 46 دقیقه و 45 ثانیه تنظیم شده است. این مقدار به ثانیه تبدیل می‌شود تا به راحتی در کد استفاده شود.

3-Description of the third part const timerElement = document.getElementById('timer');:

This line of code refers to the HTML element with the timer ID. This element is where the amount of remaining time is displayed.

3- توضیحات بخش سوم const timerElement = document.getElementById('timer');:

این خط کد به عنصر HTML با شناسه timer اشاره می‌کند. این عنصر همان جایی است که مقدار زمان باقی‌مانده نمایش داده می‌شود.

4-Description of section 4 const progressBar = document.querySelector('.progress-bar');:

این خط کد به عنصر HTML با کلاس progress-bar اشاره می‌کند. این عنصر همان جایی است که نوار پیشرفت به‌روزرسانی می‌شود.

4-توضیحات بخش چهارم const progressBar = document.querySelector('.progress-bar');:

این خط کد به عنصر HTML با کلاس progress-bar اشاره می‌کند. این عنصر همان جایی است که نوار پیشرفت به‌روزرسانی می‌شود.

5-Description of the fifth section (const initialTotalSeconds = totalSeconds;:)

In this line, the initial value of totalSeconds is saved for later use in progress bar calculations.

5-توضیحات بخش پنجم const initialTotalSeconds = totalSeconds;:

در این خط، مقدار اولیه totalSeconds ذخیره می‌شود تا بعداً در محاسبات نوار پیشرفت استفاده شود.

6-Description of the sixth section(let currentSeconds = totalSeconds;:)

This variable holds the number of seconds remaining on the timer. It is initially set to totalSeconds.

6-توضیحات بخش شیشم(let currentSeconds = totalSeconds;:)

این متغیر مقدار ثانیه‌های باقی‌مانده تایمر را نگه می‌دارد. در ابتدا برابر با totalSeconds تنظیم می‌شود.

7-Description of the seventh section(function updateTimer() { ... }:)

This function handles updating the timer and progress bar.

7-توضیحات بخش هفتم (function updateTimer() { ... }:)

این تابع به‌روزرسانی تایمر و نوار پیشرفت را مدیریت می‌کند.

8-Description of the eighth section(if (currentSeconds > 0) { ... }:)

This condition checks if there is still time left. If yes, the timer continues.

8-توضیحات بخش هشتم(if (currentSeconds > 0) { ... }:)

این شرط بررسی می‌کند که آیا هنوز زمانی باقی مانده است یا نه. اگر بله، تایمر به کار خود ادامه می‌دهد.

9-Description of the ninth section(currentSeconds--;:)

In this line, the number of seconds remaining in the timer is decreased by one unit.

9-توضیحات بخش نهم(currentSeconds--;:)

در این خط، مقدار ثانیه‌های باقی‌مانده تایمر یک واحد کاهش می‌یابد.

10-Description of the tenth section(const hours = Math.floor(currentSeconds / 3600);:
)

The number of remaining hours is calculated.

10-توضیحات بخش دهم(const hours = Math.floor(currentSeconds / 3600);:
)

تعداد ساعت‌های باقی‌مانده محاسبه می‌شود.

11-Description of the eleventh section(const minutes = Math.floor((currentSeconds % 3600) / 60);:
)

The number of minutes remaining is calculated. First, the remainder of dividing the remaining seconds by 3600 (that is, the number of seconds remaining after removing the hours) is calculated, and then it is divided by 60.

11-توضیحات بخش یازدهم(const minutes = Math.floor((currentSeconds % 3600) / 60);:
)

تعداد دقیقه‌های باقی‌مانده محاسبه می‌شود. ابتدا باقیمانده تقسیم ثانیه‌های باقی‌مانده بر 3600 (یعنی تعداد ثانیه‌های باقی‌مانده پس از حذف ساعت‌ها) محاسبه شده و سپس بر 60 تقسیم می‌شود.

12-Description of the twelfth section(const seconds = currentSeconds % 60;:
)

The number of seconds remaining is calculated.

12-توضیحات بخش دوازدهم(const seconds = currentSeconds % 60;:
)

تعداد ثانیه‌های باقی‌مانده محاسبه می‌شود.

13-Description of the thirteenth section(timerElement.textContent = ${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')};:
)

This line of code assigns the remaining hours, minutes, and seconds as a formatted string to the timerElement element. The padStart method is used to add leading zeros to single digit values ​​in HH:MM format be preserved

13-توضیحات بخش سیزدهم(timerElement.textContent = ${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')};:
)

این خط کد مقدار ساعت‌ها، دقیقه‌ها و ثانیه‌های باقی‌مانده را به صورت یک رشته فرمت شده به عنصر timerElement تخصیص می‌دهد. از متد padStart برای اضافه کردن صفر پیش از مقادیر تک‌رقمی استفاده شده است تا فرمت HH:MM
حفظ شود.

14-Description of the fourteenth section(const progressPercentage = ((initialTotalSeconds - currentSeconds) / initialTotalSeconds) * 100;:
)

This line of code calculates the progress bar percentage. This percentage is equal to the number of seconds that have elapsed divided by the total number of seconds, multiplied by 100.

14-توضیحات بخش چهاردهم(const progressPercentage = ((initialTotalSeconds - currentSeconds) / initialTotalSeconds) * 100;:
)

15-Description of the fifteenth section(progressBar.style.width = ${progressPercentage}%;:
)

The width of the progress bar is updated using the calculated value.

15-توضیحات بخش پانزدهم(progressBar.style.width = ${progressPercentage}%;:
)

عرض نوار پیشرفت با استفاده از مقدار محاسبه‌شده به‌روزرسانی می‌شود.

16-Description of the sixteenth section(setTimeout(updateTimer, 1000);:
)

This line of code calls the updateTimer function again after one second (1000 milliseconds). This will cause the timer to update every second.
updateTimer();:

16-توضیحات بخش شانزدهم(setTimeout(updateTimer, 1000);:
)

این خط کد تابع updateTimer را دوباره پس از یک ثانیه (1000 میلی‌ثانیه) فراخوانی می‌کند. این کار باعث می‌شود تایمر هر ثانیه به‌روزرسانی شود.
updateTimer();:
