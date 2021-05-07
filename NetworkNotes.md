Video https://youtu.be/k6JTaFE7SYI
## Network's dangers
- Duplication
- Reordering
- Loss 

### Solutions
Sequence number (Duplication, Reordering)

AckMsk: 11111111101b (Loss)

### RTT measurment:

C -> S (Time 1000)
S received a packet (Time 1050)
S -> C (Time 1080) We have to send time on server in packet (Tim: 30)
C received a packet (Time 1130)

**RTT** = 1130 - 1000 - 30 = 100

A ping may not be identical to the round-trip time. It differs in that most ping tests are executed within the transport protocol using ICMP packets. In contrast, RTT is measured at the application layer and includes the additional processing delay produced by higher level protocols and applications (e.g. HTTPS).


### Prediction

Client and server have a same code for prediction. By using N previous states client try to predict next state. Then server predicted the state too and substract it from real state: **RealState - PredictedState = DeltaState**

Server ---DeltaState--> Client

Client calculated RealState: **RealState = PredictedState - DeltaState**
