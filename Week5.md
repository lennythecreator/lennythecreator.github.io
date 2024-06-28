---
layout: post
title: Week 5
author: Lenny Uwaeme
---
This week was a really interesting week because I had the chance to implement the speech recognition into the application. Not only that I finally had a chance to deploy a live chat program on to render.
# What I accomplished this week

- I used the Web API to integerate text the speech in our front end it was really nice to see how techonolgies I use day to day be shown in my own project
  ```
  if (!SpeechRecognition) {
  alert("Web Speech API is not supported by this browser. Please use Chrome.");
  } else{
    const recognition = new SpeechRecognition();
    recognition.continuous = false;  // Stops automatically when the user stops speaking
    recognition.interimResults = false;  // No interim results
  
    recordButton.addEventListener('click',()=>{
      recognition.start()
    })
  
  
    recognition.onresult = (event) => {
      const transcript = event.results[0][0].transcript;
      textInput.value += transcript + '\n';
      console.log(transcript)
  }
  ```
- I was able to go through the deployment of the web app 
  ```
  @app.route('/')
  def index():
      return send_from_directory(app.template_folder, 'index.html')
  
  @app.route('/<path:filename>')
  def serve_static_files(filename):
      return send_from_directory(app.static_folder, filename)
  
  @app.route('/Styles/<path:filename>')
  def serve_styles(filename):
      return send_from_directory(app.static_folder + '/Styles', filename)

  ```
- I was able to work on my presentation skills by presenting to the high school students who came to visit.
