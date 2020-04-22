## happy path
* greet
  - utter_greet
* get_horoscope{"horoscope_sign": "capricorn"}
  - slot{"horoscope_sign": "capricorn"}
  - action_horoscope_sign
  - utter_subscribe
* subscription{"subscribe": "True"}
  - slot{"subscribe": "True"}
  - subscribe_user
* mood_great
  - utter_happy
  
## get direct horoscope with entites
* get_horoscope{"horoscope_sign": "capricorn"}
  - slot{"horoscope_sign": "capricorn"}
  - action_horoscope_sign
  - utter_subscribe
* subscription{"subscribe": "False"}
  - slot{"subscribe": "True"}
  - subscribe_user
* mood_great
  - utter_happy

## subscription  
* subscription
  - utter_subscribe
* subscription{"subscribe": "True"}
  - slot{"subscribe": "True"}
  - subscribe_user
* mood_great
  - utter_happy
  
## greet
* greet
  - utter_greet
  
## bye
* mood_great
  - utter_happy

## get horoscope  
* greet
  - utter_greet
* get_horoscope
  - utter_ask_horoscope_sign
* get_horoscope{"horoscope_sign": "capricorn"}
  - slot{"horoscope_sign": "capricorn"}
  - action_horoscope_sign
* mood_great
  - utter_happy
  
## get direct horoscope
* get_horoscope
  - utter_ask_horoscope_sign
* get_horoscope{"horoscope_sign": "capricorn"}
  - slot{"horoscope_sign": "capricorn"}
  - action_horoscope_sign
* mood_great
  - utter_happy
  
## New Story

* greet
    - utter_greet
* goodbye
    - utter_goodbye
