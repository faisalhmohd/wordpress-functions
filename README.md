# WordPress Functions

Functions + Snippets that you need every single time!

> Library of functions that is not usually mentioned in Codex and examples on some common use cases.

## Contents

* Queries
  * Parent Category of Post
  * Child Categories of Parent Category
  
### Parent Category of Post

```php
$categories = get_the_category(); 
foreach($categories as $category) {
    if ( $category->parent != 0 ) {
        // Parent Category ID is $category->parent
        $parent_category = get_category($category->parent);
    } else {
        // Has no parent category
    }
}
```

### Child Categories of Parent Category

```php
$child_categories = get_categories( array( 'parent' => $parent_cat_id ) );
```