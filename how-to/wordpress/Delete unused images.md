```
for id in $(wp db query "SELECT ID FROM wp_posts WHERE post_type='attachment' AND post_parent=0" --silent --skip-column-names)
do
    wp post delete --force $id
done
```

```
wp post delete $(wp post list --post_type='attachment' --format=ids --post_parent=0)
```