void quick_sort(int *nums, int left, int right) {
    if (left > right) return;
    int x, y, z;
    x = left; y = right; z = nums[left];
    while (x < y) {
        while (x < y && nums[y] >= z) --y;
        if (x < y) nums[x++] = nums[y];
        while (x < y && nums[x] <= z) ++x;
        if (x < y)nums[y--] = nums[x];
    }
    nums[x] = z;
    quick_sort(nums, left, x - 1);
    quick_sort(nums, x + 1, right);
}

int two_sum(int *nums, int length, int target) {
    int head = 0, tail = length - 1, ans = 0;
    while (head < tail) {
        while (head < tail && nums[head] + nums[tail] < target) ++head; 
        if (head < tail) {
            ans += head;
            tail--;
        } 
    }
    ans += (head * (head + 1)) / 2;
    return ans;
}
int three_sum_smaller(int *nums, int length, int target) {
    quick_sort(nums, 0, length - 1);
    int ans = 0;
    for (int i = 0; i < length - 2; i++) {
        ans += two_sum(nums + i + 1, length - i - 1, target - nums[i]);
    }
    return ans;
}
