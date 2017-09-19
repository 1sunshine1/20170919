bool weak_equivalent(char *str1, int length1,
                     char *str2, int length2) {
    if (length1 < length2) return false;
    if (strncmp(str1, str2, length1) == 0) return true;
    if (length1 & 1) return false;
    int mid = length1 >> 1;
    bool flag = true;
    flag = weak_equivalent(str1, mid, str2, mid);
    flag = weak_equivalent(str1 + mid, mid, str2 + mid, mid);
    if (flag) return true;
    flag = weak_equivalent(str1, mid, str2 + mid, mid);
    flag = weak_equivalent(str1 + mid, mid, str2, mid);
    return flag;
}
