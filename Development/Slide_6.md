# Setting Up

For this workshop, you'll need two things
 - A text editor, we suggest Visual Studio Code, but use whatever you're comfortable with!
 - [Node.js](https://nodejs.org/en/download/). Make sure to install the `12.19.0` version. If you get a prompt about adding to path, be sure to click yes!

After it's installed, if you open your terminal and type `node -v` in your command line and you see something like `v12.10.0` Then you will know Node.js is installed correctly!

### Running the Code

To run the code locally we have a couple of easy steps

 - `cd htf-development` (to open the workshop folder)
 - `cd functions` (to open the folder with the code)
 - `npm run build` (to compile the code)
 - `npm run dev` (to start running the code)

Note: Ignore any errors mentioned about firebase at this point. It's just a warning that express detects certain uninitialized variables.
