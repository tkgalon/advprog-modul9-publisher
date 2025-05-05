# Refleksi

Nama: Muhammad Zaid Ats Tsabit <br>
NPM: 2306224410 <br>
Kelas: Advprog-B
<hr>

1. How much data does the publisher program send to the message broker in one run? <br>
Data yang akan dikirim sebanyak 5 data ke message broker.  Masing-masing message berupa instance dari struct `UserCreatedEventMessage` yang memiliki dua field: `user_id` dan `user_name`, yang bertipe `String`.

2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? <br>

URL tersebut sama karena baik publisher maupun subscriber **terhubung ke broker yang sama**, yang berjalan di mesin lokal (`localhost`) pada port `5672`, dengan username dan password default `guest:guest`. Artinya:

- **Publisher** akan mengirim pesan ke broker itu.
- **Subscriber** akan menerima pesan dari broker yang sama, selama mereka mendengarkan queue yang sama.

Dengan URL yang sama itu, komunikasi antar komponen dapat terjadi secara real-time melalui message broker tersebut.


## Message Broker: RabbitMQ
![rabbitmq publisher](/image/rabbitmq.jpeg)