
<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/damikun/React-File-DragDrop">
  <img src="images/Upload.gif" alt="Example demo" >
  </a>

  <h3 align="center">React File Drag-Drop</h3>

  <p align="center">
   Preview of file drag drop react component
  </p>
    <p align="center">
   This is frontend file dropper include axios under the hood for sending file and receiving its token. Token is used as temporary user and file identifier and is generated by backend app. For frontend component ussage is not necessary, it is just ilustrating the full concept of uploading files for app.
  </p>
  

</p>


<!-- ABOUT -->
### About full process
- This repo contains only Frontend component (is a component trim of personal UI lib)

<p align="center">
  <a href="https://github.com/damikun/React-File-DragDrop">
    <img src="images/fileProcess.png" alt="Example demo" >
  </a>
  
  <p align="center">
   Custom project file upload process
  </p>
</p>


##### Description

The image describe simplified version of file upload handling for custom system...

This componnent helps to push file over API to backend to get tmp file token which is used to commit file using form...

##### Concepts
- Just poit it to API and get result
- Self managed component
- Ability to cancle request in flight
- Process indicator
- Validate file types on drop based on "accept" input string

##### Other
- Using Tailwind you can style it in your way
- Using PurgeCss by default
- Using functional components and hooks

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/damikun/React-File-DragDrop.git
   ```
2. CD to project dir
   ```sh
   cd .\File-DragDropper\
   ```
3. Restore packages
   ```
   yarn install
   ```
4. Build and run demo
   ```
   yarn run start
   ```
   
<!-- USAGE EXAMPLES -->
### Configuration API

   ```js
    <FileDragDrop
      className="text-gray-600"
      accept="image/png"
      multiple={false}
      api_url="https://localhost:5001/api/Data/UploadFile"

      onSuccess={(token, response) => {
        setstate(token);
      }}

      onError={(type, message, object) => {
        window.alert(`Type: ${type}, Messagbe: ${type}, Object: ${object}`)   
        if (type === "Exception") console.log(object);
        setstate("");
      }}
    />
   ```


