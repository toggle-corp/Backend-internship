# Task: Book Store Application

## Objective:
Develop a Book Store application using Django and Django REST Framework that includes user authentication with token-based authentication and email verification. Allow authenticated users to add books, retrieve their own books, and ensure secure API endpoints for these operations.

## Requirements:

### Django rest framework
 -  Proper project setup (https://github.com/susilnem/Sample-Boilerplate-drf)
### User Management and Authentication:

- Implement user registration (POST /api/register/) where users can sign up with a unique email address and password.
- Upon registration, send a verification email containing a verification link that users must click to activate their account.
- Implement a token retrieval endpoint (POST /api/token/) for users to obtain a token using their verified email and password.
- Implement a token revocation endpoint (POST /api/logout/) to invalidate a user's token and log them out.
- To implement a user info endpoint (GET /api/me) for retrieving user-specific information

### Email Verification:

- Include an endpoint (GET /api/verify-email/<verification_token>/) where users can verify their email address after clicking the verification link.
- Ensure that only verified users can retrieve tokens and access authenticated endpoints.

### Change Password
- Implement a password change endpoint (GET /api/change-password) that includes an email verification process

### Book Management:

- Implement CRUD operations for books using RESTful API endpoints (POST /api/books/, GET /api/books/, GET /api/books/<id>/, PUT /api/books/<id>/, DELETE /api/books/<id>/).
    - Delete should be soft delete
    - Only active book should allow to view
    
- Ensure that only authenticated users can add, update, and delete books.
- Users should only be able to view and manage books that they have added.
- User should able to favourite the book. make sure that user should not able to add duplicate book in favourite section
    - only user can view their fav books

### Review Management System:
- Implement a endpoint (POST /api/book/review) for review the book
- User should able to review the book

### For Token Authentication:

- Use Django REST Framework's TokenAuthentication for securing API endpoints that require authentication.
- Implement proper token management, including token expiration and refresh capabilities if necessary.
- Implement proper error handling for expired tokens, unauthorized access attempts, and unverified users.