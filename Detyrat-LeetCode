#include <iostream>
#include <vector>
#include <stack>
#include <algorithm> 
#include <map> 
#include <unordered_map> 

using namespace std;


struct ListNode {
    int val;
    ListNode* next;
    ListNode(int x) : val(x), next(nullptr) {}
};

struct TreeNode {
    int val;
    TreeNode* left;
    TreeNode* right;
    TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
};

class LinkedList1 { // Convert Binary Number in a Linked List to Integer
public:
    // Time Complexity: O(n), Space Complexity: O(n)
    int getDecimalValue(ListNode* head) {
        ListNode* temp = head;
        vector<int> vektori;
        while (temp != NULL) {
            vektori.push_back(temp->val);
            temp = temp->next;
        }
        int ans = 0;
        for (int i = vektori.size() - 1; i >= 0; i--) {
            if (vektori[i] == 0)
                continue;
            else
                ans += pow(2, vektori.size() - i - 1);
        }
        return ans;
    }
};

class LinkedList2 { // Middle of the Linked List
public:
    // Time Complexity: O(n), Space Complexity: O(1)
    ListNode* middleNode(ListNode* head) {
        int i = 0;
        ListNode* lista = head;
        while (lista != NULL) {
            lista = lista->next;
            i++;
        }
        int ans = i / 2;
        ListNode* temp = head;
        int j = 0;
        while (j < ans) {
            temp = temp->next;
            j++;
        }
        return temp;
    }
};

class LinkedList3 { // Reverse Linked List
public:
    // Time Complexity: O(n), Space Complexity: O(1)
    ListNode* reverseList(ListNode* head) {
        ListNode* previous = nullptr;
        ListNode* current = head;
        while (current != nullptr) {
            ListNode* nextTemp = current->next;
            current->next = previous;
            previous = current;
            current = nextTemp;
        }
        return previous;
    }
};

class LinkedList4 { // Remove Duplicates from Sorted List
public:
    // Time Complexity: O(n), Space Complexity: O(1)
    ListNode* deleteDuplicates(ListNode* head) {
        if (head == NULL || head->next == NULL) {
            return head;
        }
        ListNode* a = head;
        ListNode* b = head->next;
        while (b != NULL) {
            while (b != NULL && b->val == a->val) {
                b = b->next;
            }
            a->next = b;
            a = b;
            if (b != NULL) {
                b = b->next;
            }
        }
        return head;
    }
};

class LinkedList5 { // Remove Linked List Elements
public:
    // Time Complexity: O(n), Space Complexity: O(1)
    ListNode* removeElements(ListNode* head, int value) {
        if (head == NULL) {
            return NULL;
        }
        if ((head->next == NULL) && (head->val == value)) {
            return NULL;
        }
        if ((head->val != value) && (head->next == NULL)) {
            return head;
        }
        while ((head != NULL) && (head->val == value)) {
            ListNode* temp1 = head;
            head = head->next;
            temp1->next = NULL;
            delete temp1;
        }
        ListNode* temp = head;
        while ((temp != NULL) && (temp->next != NULL)) {
            ListNode* forward = temp->next;
            if (temp->next->val == value) {
                temp->next = forward->next;
                forward->next = NULL;
                delete forward;
            }
            else {
                temp = temp->next;
                forward = forward->next;
            }
        }
        return head;
    }
};

class Stack1 { // Final Prices With a Special Discount in a Shop
public:
    // Time Complexity: O(n^2), Space Complexity: O(n)
    vector<int> finalPrices(vector<int>& cmimet) {
        vector<int> ans;
        for (int i = 0; i < cmimet.size(); i++) {
            bool zbritja = false;
            for (int j = i + 1; j < cmimet.size(); j++) {
                if (cmimet[i] >= cmimet[j]) {
                    int temp = cmimet[i] - cmimet[j];
                    ans.push_back(temp);
                    zbritja = true;
                    break;
                }
            }
            if (!zbritja) {
                ans.push_back(cmimet[i]);
            }
        }
        return ans;
    }
};

class Stack2 { // Remove All Adjacent Duplicates In String
public:
    // Time Complexity: O(n), Space Complexity: O(n)
    string removeDuplicates(string s) {
        stack<char> steku;
        for (int i = 0; i < s.length(); i++) {
            char ch = s[i];
            if (steku.empty()) {
                steku.push(ch);
            }
            else if (steku.top() == ch) {
                steku.pop();
            }
            else {
                steku.push(ch);
            }
        }
        string str;
        while (!steku.empty()) {
            str = steku.top() + str;
            steku.pop();
        }
        return str;
    }
};
class Stack3 { // Make The String Great
public:
    // Time Complexity: O(n), Space Complexity: O(n)
    string makeGood(string s) {
        stack<char> stack;

        for (int i = 0; i < s.length(); i++) {
            char c = s[i];
            if (!stack.empty() && abs(c - stack.top()) == 32) {
                stack.pop();
            }
            else {
                stack.push(c);
            }
        }

        string result;
        while (!stack.empty()) {
            result = stack.top() + result;
            stack.pop();
        }

        return result;
    }
}; 


class Stack4 { // Maximum Nesting Depth of the Parentheses
public:
    // Time Complexity: O(n), Space Complexity: O(1)
    int maxDepth(string s) {
        int maksimumi_depth = 0;
        int current_depth = 0;
        for (int i = 0; i < s.size(); ++i) {
            char c = s[i];
            if (c == '(') {
                current_depth++;
            }
            if (c == ')') {
                maksimumi_depth = max(maksimumi_depth, current_depth);
                current_depth--;
            }
        }
        return maksimumi_depth;
    }
};

class Stack5 { // Remove Outermost Parentheses
public:
    // Time Complexity: O(n), Space Complexity: O(n)
     string removeOuterParentheses(string S) {
        string rezultati;
                int numruesi = 0;
        for (char c : S) {
            if (c == '(' && numruesi++ > 0) {
                rezultati += c;
            }
            if (c == ')' && numruesi-- > 1) {
                rezultati += c;
            }
        }
        return rezultati;
    }
};

class BinarySearchTree1 { // Range Sum of BST
public:
    // Time Complexity: O(n), Space Complexity: O(h) 
    int rangeSumBST(TreeNode* root, int low, int high) {
        if (root == NULL) {
            return 0;
        }
        int curr = ((low <= root->val) && (root->val <= high)) ? root->val : 0;
        int left = rangeSumBST(root->left, low, high);
        int right = rangeSumBST(root->right, low, high);
        return curr + left + right;
    }
}; 

class BinarySearchTree2 { // Search in a Binary Search Tree
public:
    // Time Complexity: O(h), Space Complexity: O(1)
    TreeNode* searchBST(TreeNode* root, int val) {
        if (root == nullptr || root->val == val) {
            return root;
        }
        if (val < root->val) {
            return searchBST(root->left, val);
        }
        return searchBST(root->right, val);
    }
};

class BinarySearchTree3 {  // All Elements in Two Binary Search Trees
public:
    // Time Complexity: O(n1 + n2), Space Complexity: O(n1 + n2)
    vector<int>ans;
    void tree(TreeNode* toot) {
        if (!toot) {
            return;
        }
        ans.push_back(toot->val);
        tree(toot->right);
        tree(toot->left);
    }
    vector<int> getAllElements(TreeNode* root1, TreeNode* root2) {
        tree(root1);
        tree(root2);
        sort(ans.begin(), ans.end());
        return ans;
    }
};

class BinarySearchTree4 { // Convert Sorted Array to Binary Search Tree
public:
    // Time Complexity: O(n), Space Complexity: O(n)
    TreeNode* solve(vector<int>& nums, int low, int high) {
        if (low <= high) {
            int mid = low + (high - low) / 2;
            TreeNode* root = new TreeNode(nums[mid]);
            root->left = solve(nums, low, mid - 1);
            root->right = solve(nums, mid + 1, high);
            return root;
        }
        return nullptr;
    }
    TreeNode* sortedArrayToBST(vector<int>& nums) {
        return solve(nums, 0, nums.size() - 1);
    }
};

class BinarySearchTree5 { // Minimum Distance Between BST Nodes
public:
    // Time Complexity: O(n), Space Complexity: O(n)
     void diff(TreeNode* root, vector<int>& arr)
     {
         if (root == NULL)
         {
             return;
         }
         diff(root->left, arr);
         arr.push_back(root->val);
         diff(root->right, arr);
     }
     int minDiffInBST(TreeNode* root)
     {
         vector<int>arr;
         diff(root, arr);
         int min1, min2 = INT_MAX;
         for (int i = 0; i < arr.size() - 1; i++)
         {
             min1 = arr[i + 1] - arr[i];
             if (min1 <= min2)
             {
                 min2 = min1;
             }
         }
         return min2;

     }
};


class HashTable1 { // Permutation Difference between Two Strings
public:
    // Time Complexity: O(n), Space Complexity: O(n)
    int findPermutationDifference(string s, string t) {
        unordered_map<char, int> mp;
        for (int i = 0; i < t.length(); i++) {
            mp[t[i]] = i;
        }
        int res = 0;
        for (int i = 0; i < s.length(); i++) {
            res += abs(i - mp[s[i]]);
        }
        return res;
    }
};

class HashTable2 {  //Number of Good Pairs
public:
    // Time Complexity: O(n), Space Complexity: O(n)
    int numIdenticalPairs(vector<int>& nums) {
        map<int, int>mp;
        int result = 0;

        for (int i : nums) {
            if (mp.count(i)) {
                result += mp[i];
            }
            mp[i]++;
        }
        return result;
    }
};

class HashTable3 {  //  Jewels and Stones
public:
    // Time Complexity: O(m + n), Space Complexity: O(m)
    int numJewelsInStones(string jewels, string stones) {
        unordered_map<char, int> map;
        int count = 0;
        for (int i = 0; i < jewels.length(); i++) {
            map[jewels[i]]++;
        }

        for (auto x : stones) {
            if (map.find(x) != map.end()) {
                count++;
            }
        }
        return count;

    }
};

class HashTable4 {  // How Many Numbers Are Smaller Than the Current Number
public:
    // Time Complexity: O(nlogn), Space Complexity: O(n)
    vector<int> smallerNumbersThanCurrent(vector<int>& nums) {
        vector<int> ans = nums;
        unordered_map<int, int> m;
        sort(ans.begin(), ans.end());
        for (int i = nums.size() - 1; i >= 0; i--)
            m[ans[i]] = i;
        for (int i = 0; i < nums.size(); i++)
            nums[i] = m[nums[i]];
        return nums;
    }
};

class HashTable5 { // Two Sum
public:
    // Time Complexity: O(n), Space Complexity: O(n)
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> mp;

        for (int i = 0; i < nums.size(); i++) {

            if (mp.find(target - nums[i]) == mp.end())

                mp[nums[i]] = i;
            else

                return { mp[target - nums[i]], i };
        }
        return { -1, -1 };
    }
};
int main() {
    int choice;
    // Display menu
    cout << "Welcome! Please choose a class to access:" << endl;
    cout << "1. LinkedList1 (Convert Binary Number in a Linked List to Integer)" << endl;
    cout << "2. LinkedList2 (Middle of the Linked List)" << endl;
    cout << "3. LinkedList3 (Reverse Linked List)" << endl;
    cout << "4. LinkedList4 (Remove Duplicates from Sorted List)" << endl;
    cout << "5. LinkedList5 (Remove Linked List Elements)" << endl;
    cout << "6. Stack1 (Final Prices With a Special Discount in a Shop)" << endl;
    cout << "7. Stack2 (Remove All Adjacent Duplicates In String)" << endl;
    cout << "8. Stack3 (Make The String Great)" << endl;
    cout << "9. Stack4 (Maximum Nesting Depth of the Parentheses)" << endl;
    cout << "10. Stack5 (Remove Outermost Parentheses)" << endl;
    cout << "11. BinarySearchTree1 (Range Sum of BST)" << endl;
    cout << "12. BinarySearchTree2 (Search in a Binary Search Tree)" << endl;
    cout << "13. BinarySearchTree3 (All Elements in Two Binary Search Trees)" << endl;
    cout << "14. BinarySearchTree4 (Convert Sorted Array to Binary Search Tree)" << endl;
    cout << "15. BinarySearchTree5 (Minimum Distance Between BST Nodes)" << endl;
    cout << "16. HashTable1 (Permutation Difference between Two Strings)" << endl;
    cout << "17. HashTable2 (Number of Good Pairs)" << endl;
    cout << "18. HashTable3 (Jewels and Stones)" << endl;
    cout << "19. HashTable4 (How Many Numbers Are Smaller Than the Current Number)" << endl;
    cout << "20. HashTable5 (Two Sum)" << endl;

    cout << "Enter your choice (1-20): ";
    cin >> choice;

    switch (choice) {
        case 1: {
            // LinkedList1
            ListNode* head = nullptr;
            LinkedList1 ll1;
            int value;
            cout << "Enter values for linked list nodes (enter -1 to stop): ";
            while (cin >> value && value != -1) {
                ListNode* newNode = new ListNode(value);
                newNode->next = head;
                head = newNode;
            }
            int decimalValue = ll1.getDecimalValue(head);
            cout << "Decimal value of binary linked list: " << decimalValue << endl;
            break;
        }
        case 2: {
            // LinkedList2
            ListNode* head = nullptr;
            LinkedList2 ll2;
            int value;
            cout << "Enter values for linked list nodes (enter -1 to stop): ";
            while (cin >> value && value != -1) {
                ListNode* newNode = new ListNode(value);
                newNode->next = head;
                head = newNode;
            }
            ListNode* middle = ll2.middleNode(head);
            if (middle) {
                cout << "Middle node value: " << middle->val << endl;
            } else {
                cout << "Linked list is empty." << endl;
            }
            break;
        }
        case 3: {
            // LinkedList3
            ListNode* head = nullptr;
            LinkedList3 ll3;
            int value;
            cout << "Enter values for linked list nodes (enter -1 to stop): ";
            while (cin >> value && value != -1) {
                ListNode* newNode = new ListNode(value);
                newNode->next = head;
                head = newNode;
            }
            ListNode* reversedHead = ll3.reverseList(head);
            cout << "Reversed linked list values: ";
            while (reversedHead != nullptr) {
                cout << reversedHead->val << " ";
                reversedHead = reversedHead->next;
            }
            cout << endl;
            break;
        }
        case 4: {
            // LinkedList4
            ListNode* head = nullptr;
            LinkedList4 ll4;
            int value;
            cout << "Enter values for sorted linked list nodes (enter -1 to stop): ";
            while (cin >> value && value != -1) {
                ListNode* newNode = new ListNode(value);
                newNode->next = head;
                head = newNode;
            }
            ListNode* newHead = ll4.deleteDuplicates(head);
            cout << "Linked list after removing duplicates: ";
            while (newHead != nullptr) {
                cout << newHead->val << " ";
                newHead = newHead->next;
            }
            cout << endl;
            break;
        }
        case 5: {
            // LinkedList5
            ListNode* head = nullptr;
            LinkedList5 ll5;
            int value, removeValue;
            cout << "Enter values for linked list nodes (enter -1 to stop): ";
            while (cin >> value && value != -1) {
                ListNode* newNode = new ListNode(value);
                newNode->next = head;
                head = newNode;
            }
            cout << "Enter value to remove: ";
            cin >> removeValue;
            ListNode* newHead = ll5.removeElements(head, removeValue);
            cout << "Linked list after removing elements: ";
            while (newHead != nullptr) {
                cout << newHead->val << " ";
                newHead = newHead->next;
            }
            cout << endl;
            break;
        }
        case 6: {
            // Stack1
            Stack1 s1;
            vector<int> prices;
            int price;
            cout << "Enter prices (enter -1 to stop): ";
            while (cin >> price && price != -1) {
                prices.push_back(price);
            }
            vector<int> finalPrices = s1.finalPrices(prices);
            cout << "Final prices after discount: ";
            for (int p : finalPrices) {
                cout << p << " ";
            }
            cout << endl;
            break;
        }
        case 7: {
            // Stack2
            Stack2 s2;
            string str;
            cout << "Enter string: ";
            cin >> str;
            string result = s2.removeDuplicates(str);
            cout << "String after removing duplicates: " << result << endl;
            break;
        }
        case 8: {
            // Stack3
            Stack3 s3;
            string str;
            cout << "Enter string: ";
            cin >> str;
            string result = s3.makeGood(str);
            cout << "String after making it good: " << result << endl;
            break;
        }
        case 9: {
            // Stack4
            Stack4 s4;
            string str;
            cout << "Enter string with parentheses: ";
            cin >> str;
            int maxDepth = s4.maxDepth(str);
            cout << "Maximum depth of parentheses: " << maxDepth << endl;
            break;
        }
        case 10: {
            // Stack5
            Stack5 s5;
            string str;
            cout << "Enter string with parentheses: ";
            cin >> str;
            string result = s5.removeOuterParentheses(str);
            cout << "String after removing outer parentheses: " << result << endl;
            break;
        }
        case 11: {
            // BinarySearchTree1
            BinarySearchTree1 bst1;
            TreeNode* root = nullptr; 
            int low, high;
            cout << "Enter range (low high): ";
            cin >> low >> high;
            int sum = bst1.rangeSumBST(root, low, high);
            cout << "Range sum of BST: " << sum << endl;
            break;
        }
        case 12: {
            // BinarySearchTree2
            BinarySearchTree2 bst2;
            TreeNode* root = nullptr; 
            int val;
            cout << "Enter value to search: ";
            cin >> val;
            TreeNode* result = bst2.searchBST(root, val);
            cout << "Search result: " << (result ? "Found" : "Not Found") << endl;
            break;
        }
        case 13: {
            // BinarySearchTree3
            BinarySearchTree3 bst3;
            TreeNode* root1 = nullptr; 
            TreeNode* root2 = nullptr; 
            vector<int> result = bst3.getAllElements(root1, root2);
            cout << "All elements from two BSTs: ";
            for (int val : result) {
                cout << val << " ";
            }
            cout << endl;
            break;
        }
        case 14: {
            // BinarySearchTree4
            BinarySearchTree4 bst4;
            vector<int> nums;
            int num;
            cout << "Enter sorted array (enter -1 to stop): ";
            while (cin >> num && num != -1) {
                nums.push_back(num);
            }
            TreeNode* root = bst4.sortedArrayToBST(nums);
            // Example: Traverse and print the BST (in-order traversal)
            cout << "BST created from sorted array." << endl;
            break;
        }
        case 15: {
            // BinarySearchTree5
            BinarySearchTree5 bst5;
            TreeNode* root = nullptr; // Example: Initialize BST manually for testing
            int minDiff = bst5.minDiffInBST(root);
            cout << "Minimum distance between BST nodes: " << minDiff << endl;
            break;
        }
        case 16: {
            // HashTable1
            HashTable1 ht1;
            string s1, s2;
            cout << "Enter first string: ";
            cin >> s1;
            cout << "Enter second string: ";
            cin >> s2;
            bool result = ht1.findPermutationDifference(s1, s2);
            cout << "Are the two strings permutations of each other? " << (result ? "Yes" : "No") << endl;
            break;
        }
        case 17: {
            // HashTable2
            HashTable2 ht2;
            vector<int> nums;
            int num;
            cout << "Enter numbers (enter -1 to stop): ";
            while (cin >> num && num != -1) {
                nums.push_back(num);
            }
            int goodPairs = ht2.numIdenticalPairs(nums);
            cout << "Number of good pairs: " << goodPairs << endl;
            break;
        }
        case 18: {
            // HashTable3
            HashTable3 ht3;
            string jewels, stones;
            cout << "Enter jewels: ";
            cin >> jewels;
            cout << "Enter stones: ";
            cin >> stones;
            int numJewels = ht3.numJewelsInStones(jewels, stones);
            cout << "Number of jewels in stones: " << numJewels << endl;
            break;
        }
        case 19: {
            // HashTable4
            HashTable4 ht4;
            vector<int> nums;
            int num;
            cout << "Enter numbers (enter -1 to stop): ";
            while (cin >> num && num != -1) {
                nums.push_back(num);
            }
            vector<int> result = ht4.smallerNumbersThanCurrent(nums);
            cout << "Count of smaller numbers than each element: ";
            for (int val : result) {
                cout << val << " ";
            }
            cout << endl;
            break;
        }
        case 20: {
            // HashTable5
            HashTable5 ht5;
            vector<int> nums;
            int num, target;
            cout << "Enter numbers (enter -1 to stop): ";
            while (cin >> num && num != -1) {
                nums.push_back(num);
            }
            cout << "Enter target sum: ";
            cin >> target;
            vector<int> result = ht5.twoSum(nums, target);
            cout << "Indices of two numbers that add up to target: ";
            for (int idx : result) {
                cout << idx << " ";
            }
            cout << endl;
            break;
        }
        default:
            cout << "Invalid choice. Please enter a number between 1 and 20." << endl;
            break;
    }

    return 0;
}