# Bridge
![image](https://github.com/Pillar-Bridge/bridge/assets/71630722/6d3d5f5b-bd90-489f-b4ec-02b8d0afc9ca)

This is a project that participated in the 2024 Google Solution Challenge.


# Member
The team name that developed the **Bridge** project is **Pillar**.

| **Gyeongrok Kim** | **Dawon Seo** | **Mirae Kim** | **Daehyeon Choi** |
| :---------------: | :-----------: | :-----------: | :---------------: |
| [<img src="https://github.com/gomsang.png" height=100 width=100><br/>@gomsang](https://github.com/gomsang) | [<img src="https://github.com/Dawon00.png" height=100 width=100><br/>@Dawon00](https://github.com/Dawon00) | [<img src="https://github.com/FutureandKim.png" height=100 width=100><br/>@FutureandKim](https://github.com/FutureandKim) | [<img src="https://github.com/dablro12.png" height=100 width=100><br/>@dablro12](https://github.com/dablro12) |
| Lead <br/> Frontend | Frontend | Backend | AI |


# Target UN-SDGs
![image](https://github.com/Pillar-Bridge/bridge/assets/71630722/646a8767-06a5-4a25-a741-f9c0a7c403d1)

# About our solution
'Bridge' is an AI assistant solution designed to help individuals with language disabilities overcome communication barriers in medical and everyday situations. </br>
It integrates advanced natural language processing algorithms and AI to accurately interpret user intentions and generate appropriate responses. </br>
This reduces medical diagnostic errors, improves the quality of life for people with language development disorders, and facilitates education and social participation. </br>
'Bridge' combines real-time speech recognition and location-based services to enable real-time translation and voice conversion into various languages, supporting effective communication in daily life for individuals with language disabilities.



# App Demo
<img src="https://github.com/Pillar-Bridge/bridge/assets/71630722/2755a284-27b1-4c3f-a523-bf8d55fa4ffe" width="400" />
<img src="https://github.com/Pillar-Bridge/bridge/assets/71630722/c8dcf228-9035-4112-adbe-e0d320b3a998" width="400" />
<img src="https://github.com/Pillar-Bridge/bridge/assets/71630722/931e7855-43c5-49a9-93cf-66404365c92b" width="400" />
<img src="https://github.com/Pillar-Bridge/bridge/assets/71630722/f5214bb2-be7e-441b-ae20-5a8bf9c29037" width="400" />

# About Implementation
![image](https://github.com/Pillar-Bridge/bridge/assets/71630722/21c11ef5-abba-45ad-8b19-ccecc80eac8c)

## Frontend
### 1. Tech Stack
- Dart SDK: 3.2.6
- Flutter SDK: Compatible with version >=3.2.6 <4.0.0
- geolocator: 11.0.0
- just_audio: 0.9.36
- path_provider: 2.1.2
- record: 5.0.4
- shared_preferences: 2.2.2
- speech_to_text: 6.6.0
  
### 2. Architecture
```
lib
 ┣ api
 ┃ ┣ responses
 ┃ ┃ ┣ api_response.dart
 ┃ ┃ ┣ res_replies.dart
 ┃ ┃ ┣ res_dialogue.dart
 ┃ ┃ ┣ res_message_dialogue.dart
 ┃ ┃ ┣ res_modification_options.dart
 ┃ ┃ ┗ res_place_recommendation.dart
 ┃ ┗ api_client.dart
 ┣ controllers
 ┃ ┗ voice_recorder.dart
 ┣ models
 ┣ ui
 ┃ ┣ constants
 ┃ ┃ ┗ app_theme.dart
 ┃ ┣ screens
 ┃ ┃ ┣ TestScreen.dart
 ┃ ┃ ┣ common_widget_test_screen.dart
 ┃ ┃ ┣ full_text_screen.dart
 ┃ ┃ ┣ select_answer_screen.dart
 ┃ ┃ ┣ select_place_screen.dart
 ┃ ┃ ┣ stt_test_screen.dart
 ┃ ┃ ┣ voice_recognition_screen.dart
 ┃ ┃ ┗ voice_setting_screen.dart
 ┃ ┗ widgets
 ┃ ┃ ┣ buttons
 ┃ ┃ ┃ ┣ button_basic.dart
 ┃ ┃ ┃ ┣ button_basic_icon.dart
 ┃ ┃ ┃ ┣ button_current_situation.dart
 ┃ ┃ ┃ ┣ button_select_sentence.dart
 ┃ ┃ ┃ ┣ button_suggestion_sentence.dart
 ┃ ┃ ┃ ┣ button_toggle_icon.dart
 ┃ ┃ ┃ ┣ button_toggle_text.dart
 ┃ ┃ ┃ ┗ button_word_replacement.dart
 ┃ ┃ ┣ progresses
 ┃ ┃ ┃ ┗ progress_threedots.dart
 ┃ ┃ ┗ change_word.dart
 ┣ utils
 ┃ ┗ token_manager.dart
 ┗ main.dart

```

## Backend
### 1. Tech Stack
- Java: 17
- Spring Boot: 3.2.2
- Spring Data JPA
- MySQL
- Docker
- AWS EC2

### 2. Architecture
```
┣ main
┃   ┣ generated
┃   ┣ java
┃   ┃   ┗ com
┃   ┃       ┗ pillar
┃   ┃           ┗ bridge
┃   ┃               ┃   BridgeApplication.java
┃   ┃               ┃   
┃   ┃               ┣ apiUtils
┃   ┃               ┃   ┃   ErrorAdvice.java
┃   ┃               ┃   ┃   ResponseDto.java
┃   ┃               ┃   ┃   ResponseUtil.java
┃   ┃               ┃   ┃   
┃   ┃               ┃   ┗ codeStatus
┃   ┃               ┃           ErrorResponse.java
┃   ┃               ┃           SuccessResponse.java
┃   ┃               ┃           
┃   ┃               ┣ config
┃   ┃               ┃       AppConfig.java
┃   ┃               ┃       Constants.java
┃   ┃               ┃       
┃   ┃               ┣ controller
┃   ┃               ┃       AlterController.java
┃   ┃               ┃       DialogueController.java
┃   ┃               ┃       FullDialogueController.java
┃   ┃               ┃       PlacesController.java
┃   ┃               ┃       ReplyController.java
┃   ┃               ┃       TTSController.java
┃   ┃               ┃       UpdateMessageController.java
┃   ┃               ┃       
┃   ┃               ┣ dto
┃   ┃               ┃   ┃   PlacesDto.java
┃   ┃               ┃   ┃   RegisterResponse.java
┃   ┃               ┃   ┃   RequestModel.java
┃   ┃               ┃   ┃   TTSDto.java
┃   ┃               ┃   ┃   
┃   ┃               ┃   ┣ alter
┃   ┃               ┃   ┃       AlterRequest.java
┃   ┃               ┃   ┃       AlterResponse.java
┃   ┃               ┃   ┃       WordOption.java
┃   ┃               ┃   ┃       
┃   ┃               ┃   ┣ dialogue
┃   ┃               ┃   ┃       DialogueRequest.java
┃   ┃               ┃   ┃       DialogueResponse.java
┃   ┃               ┃   ┃       
┃   ┃               ┃   ┣ FullDialogue
┃   ┃               ┃   ┃       FullDialogueDto.java
┃   ┃               ┃   ┃       FullDialogueResponseDto.java
┃   ┃               ┃   ┃       
┃   ┃               ┃   ┣ place
┃   ┃               ┃   ┃   ┣ googleApi
┃   ┃               ┃   ┃   ┃       GoogleResponse.java
┃   ┃               ┃   ┃   ┃       PlaceResponse.java
┃   ┃               ┃   ┃   ┃       PlacesRequest.java
┃   ┃               ┃   ┃   ┃       
┃   ┃               ┃   ┃   ┗ kakaoApi
┃   ┃               ┃   ┃           Document.java
┃   ┃               ┃   ┃           KaKaoResponse.java
┃   ┃               ┃   ┃           Meta.java
┃   ┃               ┃   ┃           PlaceNameResponse.java
┃   ┃               ┃   ┃           SameName.java
┃   ┃               ┃   ┃           
┃   ┃               ┃   ┣ TTS
┃   ┃               ┃   ┃       TTSRequest.java
┃   ┃               ┃   ┃       TTSResponse.java
┃   ┃               ┃   ┃       
┃   ┃               ┃   ┗ UpdateMessage
┃   ┃               ┃           UpdateRequest.java
┃   ┃               ┃           UpdateResponse.java
┃   ┃               ┃           
┃   ┃               ┣ entitiy
┃   ┃               ┃       Device.java
┃   ┃               ┃       Dialogue.java
┃   ┃               ┃       Messages.java
┃   ┃               ┃       
┃   ┃               ┣ repository
┃   ┃               ┃       DeviceRepository.java
┃   ┃               ┃       DialogueRepository.java
┃   ┃               ┃       MessageRepository.java
┃   ┃               ┃       
┃   ┃               ┗ service
┃   ┃                   ┃   AlterService.java
┃   ┃                   ┃   DeviceService.java
┃   ┃                   ┃   DialogueService.java
┃   ┃                   ┃   FullDialogueService.java
┃   ┃                   ┃   ReplyService.java
┃   ┃                   ┃   TTSService.java
┃   ┃                   ┃   UpdateMessageService.java
┃   ┃                   ┃   
┃   ┃                   ┗ place
┃   ┃                           RecommPlaceGoogleService.java
┃   ┃                           RecommPlaceKaKAoService.java
┃   ┃                           
┃   ┗ resources
┃       ┃   application.properties
┃       ┃   
┃       ┣ static
┃       ┗ templates
┗ test
    ┗ java
        ┗ com
            ┗ pillar
                ┗ bridge
                        BridgeApplicationTests.java

```

## AI
### 1. Tech Stack

### 2. Architecture
