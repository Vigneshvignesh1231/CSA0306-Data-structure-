#include <stdio.h>
#include <stdlib.h>

struct Node {
    int key;
    int height;
    struct Node *left;
    struct Node *right;
};

int max(int a, int b);
int height(struct Node *N);
int getBalance(struct Node *N);
struct Node* newNode(int key);
struct Node* rightRotate(struct Node *y);
struct Node* leftRotate(struct Node *x);
struct Node* insert(struct Node* node, int key);
struct Node* deleteNode(struct Node* root, int key);
struct Node * minValueNode(struct Node* node);
void preOrder(struct Node *root);
struct Node* search(struct Node* root, int key);

int main() {
    struct Node *root = NULL;
    root = insert(root, 10);
    root = insert(root, 20);
    root = insert(root, 30);
    root = insert(root, 40);
    root = insert(root, 50);
    root = insert(root, 25);

    printf("Preorder traversal of the constructed AVL tree is \n");
    preOrder(root);

    root = deleteNode(root, 30);

    printf("Preorder traversal after deletion of 30 \n");
    preOrder(root);

    struct Node *result = search(root, 40);
    if (result == NULL)
        printf("40 Not Found\n");
    else
        printf("40 Found\n");

    return 0;
}

int max(int a, int b) {
    return (a > b)? a : b;
}

int height(struct Node *N) {
    if (N == NULL)
        return 0;
    return N->height;
}

int getBalance(struct Node *N) {
    if (N == NULL)
        return 0;
    return height(N->left) - height(N->right);
}

struct Node* newNode(int key) {
    struct Node* node = (struct Node*)
                        malloc(sizeof(struct Node));
    node->key   = key;
    node->left   = NULL;
    node->right  = NULL;
    node->height = 1;
    return(node);
}

struct Node* rightRotate(struct Node *y) {
    struct Node *x = y->left;
    struct Node *T2 = x->right;

    x->right = y;
    y->left = T2;

    y->height = max(height(y->left), height(y->right))+1;
    x->height = max(height(x->left), height(x->right))+1;

    return x;
}

struct Node* leftRotate(struct Node *x) {
    struct Node *y = x->right;
    struct Node *T2 = y->left;

    y->left = x;
    x->right = T2;

    x->height = max(height(x->left), height(x->right))+1;
    y->height = max(height(y);
