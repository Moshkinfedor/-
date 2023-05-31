import java.util.Scanner;

public class CircularArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the number of elements in the array: ");
        int n = sc.nextInt();
        System.out.print("Enter the interval length: ");
        int m = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = i + 1;
        }
        int current = 0;
        System.out.print("Path: ");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[current]);
            current = (current + m) % n;
        }
    }
}
[code:]java[:code]




private Point calculateCenterCircleSmall(int sizeCircle, Point center, double angle)




{




//x0,y0 - центр, a - угол, r - радиус.




int radius = sizeCircle / 2;




int x = (int) (center.x + radius * Math.cos(Math.toRadians(angle)));




int y = (int) (center.y + radius * Math.sin(Math.toRadians(angle)));




return new Point(x, y);




}








[/code]
Часть структуры tests.json:
{"id": 122, "title": "Security test", "value": "", "values":
[{"id": 5321, "title": "Confidentiality", "value": ""},
{"id": 5322, "title": "Integrity", "value": ""}]}

После заполнения в соответствии с values.json:
{"values": [{"id": 122, "value": "failed"}, {"id": 5321,"value": "passed"}, {"id": 5322,"value": "failed"}]}

Будет иметь следующий вид в файле report.json:
{"id": 122, "title": "Security test", "value": "failed", "values":
[{"id": 5321, "title": "Confidentiality", "value": "passed"},
{"id": 5322, "title": "Integrity", "value": "failed"}]}
import math

nums = [1, 10, 2, 9]
result_digit = math.ceil((max(nums))/2)
count = 0
for id, i in enumerate(nums):
    while i != result_digit:
         if i < result_digit:
             i += 1
             count += 1
         elif i > result_digit:
              i -= 1
              count += 1
         else:
            nums[id] = i
    print(count)
