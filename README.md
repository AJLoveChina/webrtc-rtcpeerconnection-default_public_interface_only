# webrtc-rtcpeerconnection-default_public_interface_only
Microsoft Edge set Policy Name : WebRtcLocalhostIpHandling=>default_public_interface_only, How to create local peer to peer connection in the same webpage?


## Stackoverflow issue Link
https://stackoverflow.com/questions/63294777/webrtclocalhostiphandling-policy-makes-webrtc-peerconnection-not-working


## Online Demo Page
https://ajlovechina.github.io/webrtc-rtcpeerconnection-default_public_interface_only/.


## Issue Description

There is a webrtc example from WebRTC org

https://webrtc.github.io/samples/src/content/peerconnection/pc1/

It shows how to create Peer Connection between two peers. However, it is important to note that both peers are on the local computer. And this is also what we want, we need this peerConnection to gain AEC(audio echo cancel) benefit.

But in the network environment of our school, We only use Edge(Chromium) to join webrtc webpage. And for safety reasons, we set **WebRtcLocalhostIpHandling** to **default_public_interface_only**, which makes the rtcpeerConnection broken, not working.

Let me explain: WebRtcLocalhostIpHandling is a policy that influence the behavior of the Edge browser. And the value default_public_interface_only means that Allows the use of a common interface over HTTP default routing.This does not expose the local IP address

Now is the question: We need the rtcpeerConnection working and also need the policy setting, what should we do? Is there some configuration for rtcPeerConnection api?

