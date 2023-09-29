## Purpose
This was our first blitz, and our primary objective was to test our Elastic Beanstalk application, specifically focusing on latency. We received customer complaints from Nike regarding slow webpage loading times, and Nike wanted us to reduce the latency to improve the user experience.

## Things that happened during Blitz
Here's a detailed account of what transpired during the blitz:

1) Application Verification: We started by confirming that our Elastic Beanstalk application named "URL Shortener" was up and running.

2) Latency Measurement: We initiated the blitz by measuring the latency of our application. It became evident that latency was indeed influenced by the geographical location of both our application and its users.

3) Geographical Impact Analysis: Further investigation revealed that our "URL Shortener" was deployed in the us-east-1 region, affecting latency for users on the west coast.

4) Initial Latency Reading: The initial measurement showed an average latency of 40.879 milliseconds, which was not meeting Nike's expectations.

5) Brainstorming Solutions: We convened to brainstorm potential solutions to reduce the latency for accessing the "URL Shortener." Our discussions covered both infrastructure and application-level changes.

6) Decision to Implement CDN: After considering various options, we collectively decided to implement a Content Delivery Network (CDN), specifically Amazon CloudFront, to address the latency issue.

7) Configuring CDN (CloudFront): We proceeded to configure Amazon CloudFront to optimize content delivery. In the configuration, we set cache key and optimization options to enhance the CDN's performance.

8) Distribution Creation: We created a distribution in Amazon CloudFront.

9) Testing CDN Configuration: To validate the effectiveness of our CDN configuration, we accessed the URL provided by the distribution, which directed us to the "URL Shortener" application.

10) Performance Test with Codeon: To quantify the improvement, we conducted a performance test using Codeon. This test revealed that the average latency had significantly decreased from 40.879 milliseconds to 9.652 milliseconds after configuring CloudFront. This represented a substantial increase in speed.

## Lessons Learned
From this blitz event, we learned several valuable lessons:

The geographical location of both the application and users plays a critical role in latency.

CDNs, like Amazon CloudFront, can effectively reduce latency by caching content closer to end-users.

Regular performance monitoring and optimization are essential for addressing user experience issues.

## Next Steps
Our plan for the next steps includes:

1) Continuous monitoring of application performance and adjusting CloudFront settings as needed to maintain low latency.

2) Considering other optimization techniques, such as further infrastructure scaling, if necessary.

## Conclusion
In conclusion, the latency reduction blitz successfully addressed the issue raised by Nike regarding slow webpage loading times. By implementing Amazon CloudFront as a CDN and optimizing content delivery, we significantly reduced latency and, in turn, improved the overall user experience. This initiative highlighted the importance of considering infrastructure and geographical factors when tackling latency issues.

## Diagram

![image](https://github.com/SaraGurungLABS01/Blitz_1/assets/140760966/6a255739-b6c3-4561-845c-229109338606)

