# Markdown
<!DOCTYPE html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="style.css">
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3"
      crossorigin="anonymous"
    />
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>

    <script src="marked.js"></script>
    <script>
      //make the code visible on the editor side
      function updatePreview() {
        let previewElement = document.getElementById("preview");
        let editorValue = document.getElementById("editor");
        previewElement.innerHTML = marked.parse(editorValue.value);
      }
      // HERE START THE MARKDOWN CODE
      function setDefault() {
        let defaultText = `
# Lorem ipsum dolor 
## Lorem ipsum dolor:
Lorem ipsum dolor sit **amet consectetur**  [consectetur][consectetur]  Ducimus.
[Lorem ipsum dolor ](https://Loremipsumdolorsit.com)
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione, pariatur a aliquam dolorum **soluta harum** minima tempore, repellat numquam tenetur aliquid dicta. Qui iste **sapiente sunt cum autem et!** Ducimus
## Lorem
- Lorem ipsum
- Lorem ipsum
- Lorem ipsum
### Lorem ipsum 
      1. Lorem ipsum dolor
      2. Lorem ipsum dolor
      3. Lorem ipsum dolor
      4. Lorem ipsum dolor
*Lorem ipsum dolor sit amet consectetur adipisicing elit. [Roman numeral four][2].*
### Lorem ipsum
* Lorem ipsum
* Lorem ipsum
* Lorem ipsum
* Lorem ipsum
<dl>
  <dt> Lorem ipsum dolor</dt>
  <dd> Lorem ipsum dolor</dd>
  <dt> Lorem ipsum dolor</dt>
  <dd> Lorem ipsum dolor</dd>
</dl>
> \`  Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione, pariatur a aliquam dolorum soluta harum minima tempore, repellat numquam tenetur aliquid dicta. Qui iste sapiente sunt cum autem et! Ducimus.
Lorem ipsum dolor sit\`
![](https://images.vexels.com/media/users/3/140692/isolated/lists/72d1f12edf758d24f5b6db73bac4f297-logo-de-linux.png)
`; //make the code visible on Preview side
        let editorField = document.getElementById("editor");
        let previewElement = document.getElementById("preview");
        editorField.value = defaultText;
        previewElement.innerHTML =marked.parse(defaultText);
      }
    </script>

    <title>Markdown</title>
  </head>
  <!--Call the funtcion Onload-->
  <body class="bg-warning bg-opacity-25" onload="setDefault()">
    <div class="container-fluid">
      <div class="row">
        <h1 class="col text-center bg-black text-white">Markdown</h1>

        <div class="row">
          <div class="col-6">
            <p class="text-center">Test your code here</p>
            <!-- Call the function to load the ''code'''-->
            <textarea
              name=""
              id="editor"
              class=" bg-white bg-opacity-75"
              onkeyup="updatePreview()"
            ></textarea>
          </div>
          <div class="col-6">
            <div id="preview">
              <p class="text-center">Code looks like:</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!--Scripts and CDN-->

    <script
      src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js"
      integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB"
      crossorigin="anonymous"
    ></script>
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js"
      integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13"
      crossorigin="anonymous"
    ></script>

    <script src="https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js"></script>
  </body>
</html>
