# ArraySorter
ArraySorter
import java.util.Arrays;

public class ArraySorter {
    public static void main(String[] args) {
        int[] array = {5, 2, 9, 1, 3};
        sortArrayDescending(array);
        System.out.println("Отсортированный массив: " + Arrays.toString(array));
    }

    public static void sortArrayDescending(int[] array) {
        int length = array.length;
        for (int i = 0; i < length - 1; i++) {
            for (int j = 0; j < length - i - 1; j++) {
                if (array[j] < array[j + 1]) {
                    int temp = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = temp;
                }
            }
        }
    }
}
