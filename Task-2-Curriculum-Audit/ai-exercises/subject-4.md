# AI-assisted exercise — Computer Networks

## Topic
TCP and UDP

## Prompt used
> Explain the difference between TCP and UDP using a simple real-world example. Describe how they differ in reliability, speed, and connection setup. Give two applications where TCP is preferred and two where UDP is preferred. Keep the explanation suitable for a B.Tech student.

## Tool and date
- **AI tool:** ChatGPT
- **Date:** 23 October 2026
- **Subject:** Computer Networks

## Summary of the response
The response compared TCP with sending a document where delivery is acknowledged and missing parts can be retransmitted, and UDP with sending packets without built-in delivery confirmation. It covered TCP connection setup, ordered reliable byte-stream delivery and higher protocol overhead, compared with UDP datagrams and no built-in retransmission. Examples included traditional web/file-transfer use for TCP and online games or real-time audio/video for UDP. It noted that HTTP/3 uses QUIC over UDP.

## Review and verification
I read the explanation and did not identify a correction to make. I did not test network traffic or independently verify each application protocol. Protocol choice depends on the application: UDP does not guarantee lower end-to-end latency, and applications can add their own reliability mechanisms.

## What I learned
I learned that TCP and UDP make different trade-offs between built-in reliability and overhead, and that the application determines which trade-off is suitable.

## Record status
The response was reviewed in this assignment session and no correction was reported. The review did not include a documented external-source check or independent practical test, so this file does not claim either one took place.
