# Keerthanabmkeerthi
struct node* insert(struct node* root, int data) {

    if (root == NULL) {
        struct node* newNode = (struct node*)malloc(sizeof(struct node));
        newNode->data = data;
        newNode->left = NULL;
        newNode->right = NULL;
        return newNode;
    }

    if (data < root->data) {
        root->left = insert(root->left, data); 
    } else {
        root->right = insert(root->right, data); 
    }

    
    return root;
}
