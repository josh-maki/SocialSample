# SocialSample
This is a sample social media application based on Kubernetes.

**It consists of several components:
**1. API gateway. Serves as intermediary between end client (user web browser) and back-end services. Displays UI. Based on Kong.
2. Authentication service. Produces JWT token so that users can log in. Based on MongoDB.
3. Friend feed service. Displays latest posts from accounts that the user is following. Based on Kafka. 
4. News feed service. Displays other trending posts at bottom of friend feed service.
5. Like service. Allows users to like items that they view.
6. Post service. Allows users to make a post (up to 80 characters, optionally with a video or image)
7. Message service. Allows users to send and receive messages from each other.
8. Logging service. Distributed logging to store logs relevant for debugging.
9. Audit logging service. For auditing data access, etc.
10. Notification service. Alerts users when close friends make a post, when one of the user's posts are liked, when the user receives a message.

**Productionization steps:
**1. Logging service.
2. Audit logging.
3. Minimal user access settings.
4. Pods only accept requests from known IPs.

**Development**
1. Folder per service contains: Kubernetes yamls. .java files.
2. CI/CD pipeline based on Jenkins
3. Dev/Stage/Main Branches
