# Flexbox
Flexbox is a way to arrange items into rows or columns, where those items will flex (i.e. grow or shrink) based on some simple rules that you can define.

## Flex Containers and Flex Items
As you’ve seen, flexbox isn’t just a single css property, but a whole toolbox of properties that you can use to put things where you need them. Some of these properties belong on the *flex container* and some go on the *flex items*.

A flex container is any element that has `display: flex` on it. A flex item is any element that lives directly inside of a flex container.
![image](https://cdn.statically.io/gh/TheOdinProject/curriculum/495704c6eb6bf33bc927534f231533a82b27b2ac/html_css/v2/foundations/flexbox/imgs/03.png)
Somewhat confusingly, any element can be both a flex container and a flex item. Said another way, you can also put `display: flex` on a flex item, and then use flexbox to arrange its children.
![image](https://cdn.statically.io/gh/TheOdinProject/curriculum/495704c6eb6bf33bc927534f231533a82b27b2ac/html_css/v2/foundations/flexbox/imgs/04.png)

This method of creating and nesting multiple flex containers and items is the primary way we will be building up complex layouts. The next image was achieved using only flexbox to arrange, size, and place the various elements. Flexbox is a very powerful tool.
![img](https://cdn.statically.io/gh/TheOdinProject/curriculum/495704c6eb6bf33bc927534f231533a82b27b2ac/html_css/v2/foundations/flexbox/imgs/05.png)
