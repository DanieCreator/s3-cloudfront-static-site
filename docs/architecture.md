## Why CloudFront Instead of Direct S3 Access?
# ( Here I explain Why S3 should not be public, Why CDN is used, and Trade-offs)
Using S3 static website hosting exposes the bucket publicly.  
In this design, CloudFront acts as a controlled access layer, allowing:
- Better security via OAC
- HTTPS enforcement
- Edge caching for performance
