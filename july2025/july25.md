### ⚡july4

- in java `i++` vs `++i`

### ⚡july11

# a level-One Heading
## a level-Two Heading
### a level-Three heading (no line seprator)
#### important Bullet Points

- one
- two
- three

#### numerical Points
1. First
2. Second
3. Thrid

#### list
 - a - dash
 * b * star
 + c + plus 

--------------------- a line
--- 
#### three dash

- __Bold__
- **BoldAgain** also __BoldAgain2__
- **This is _very_ important**
- ***Very vital therefore bold and italic***

## Link
To use a link in your presentation use `[]()` syntax   
- [a link](https://www.google.com)



## Alerts     
**Supported in some markDown preview.But surely will come up on Github preview.**

> [!NOTE]  
> Now here ,write ur remarks.

> [!CAUTION]  
> Now here ,write ur remarks.

> [!Tip]  
> Now here ,write ur remarks.

> [!Warning]  
> Now here ,write ur remarks.

> [!IMPORTANT]  
> Now here ,write ur remarks.

## codeBlockk
- either , triple backtiks` ``` ``` ` or four times`[space][space][space][space]`

```java
public class Demo{
    public static void main(String[] args){
        System.out.println("Hello Python");
    }
}
```
```python
print("Hello Python")
```
## Highlighter
here in this sentense we can ==really highlight== a word.  (not suppoeted in all)
here in this sentense we can <mark> really highlight</mark> a word.

## Images
- `![Alt text](image-url)`  

Since Markdown doesn’t support resizing images, inline HTML can be used here to accomplish this task.  
- `<img src="image-url" alt="Alt text" width="<width>" height="<height>">`    
--- 
![alt text](tiger.png)
--- 
  inCenter using html,controlling size
<!-- <center>  
<img src="tiger.png" alt="aTiger" width="100" style="border: 2px solid yellow;">
</center>    this syntax is outdated. -->
<div align="center">
<img src="tiger.png" alt="aTiger" width="100" style="border: 2px solid yellow;">
</div>

>[!IMPORTANT]  
>vsCode supports html style formatting . Therefore,u can see border style and color in vsCode but not on github.   
>In order to see these alerts properly on vsCode u need extentions such as enhanced markdown or all in one md.






