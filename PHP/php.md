# PHP

We use a MVC oriented PHP workflow. We will give certain details and why we do thing they way do.

### Folder Structure
```
App
│
├─Models
├─Views
├─Controllers
└─Libraries
```


## View Details

Usually to include the view files `require_once('fileName.php');` is often used.
We use a  different strategy for this, as we use a template class, we save the HTML content 
in a variable then we proceed to print it directly. Example:

```PHP
<body>
    <h1>
        <?php echo $title; ?>
    </h1>
    <?php echo $content; ?>
</body>
```

Here on `$content`, we would save something like the following:

```PHP
<div>
    <p> Lorem Ipsum... </p>
</div>
```

Using our template class.