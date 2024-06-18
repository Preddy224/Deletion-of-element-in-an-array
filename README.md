# Deletion-of-element-in-an-array




code 




public class Deletion {

    public static int findElement(int[] arr, int key, int N) {
        for (int i = 0; i < N; i++)
            if (arr[i] == key)
                return key;

        return -1;
    }

    public static int delete(int[] arr, int key, int N) {
        int pos = findElement(arr, key, N);
        if (pos == -1) {
            System.out.println("element not found");

            return N;
        }

        for (int i = pos; i < N - 1; i++)
            arr[i] = arr[i + 1];
        return (N - 1);

    }

    public static void main(String[] args) {
        int arr[] = { 10, 20, 30, 40, 50 };
        int key = 50;
        int N = arr.length;

        System.out.println("before deletion");
        for (int i = 0; i < N; i++) {
            System.out.println(arr[i] + " ");

        }

        N = delete(arr, key, N);

        System.out.println("after deletion");
        for (int i = 0; i < N; i++) {
            System.out.println(arr[i] + " ");

        }
    }
}
