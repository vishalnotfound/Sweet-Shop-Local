##Manual Test Report
Authentication Tests
Test Case	Steps	Expected Result	Actual Result	Status
Register User	POST /api/auth/register with new user data	Status 201, user created	Status 201, user created	✅ Pass
Login User	POST /api/auth/login with valid credentials	Status 200, returns JWT	Status 200, returns JWT	✅ Pass
Login with wrong credentials	POST /api/auth/login with invalid data	Status 401, unauthorized	Status 401, unauthorized	✅ Pass


##Sweets Management Tests
Test Case	Steps	Expected Result	Actual Result	Status
Add Sweet (Admin)	POST /api/sweets with sweet details	Status 201, sweet added	Status 201, sweet added	✅ Pass
Get All Sweets	GET /api/sweets	Status 200, list of sweets	Status 200, list returned	✅ Pass
Search Sweets	GET /api/sweets/search?name=Chocolate	List of matching sweets	List of matching sweets	✅ Pass
Update Sweet (Admin)	PUT /api/sweets/:id	Sweet details updated	Sweet details updated	✅ Pass
Delete Sweet (Admin)	DELETE /api/sweets/:id	Sweet deleted	Sweet deleted	✅ Pass


##Inventory Management Tests
Test Case	Steps	Expected Result	Actual Result	Status
Purchase Sweet	POST /api/sweets/:id/purchase	Quantity decreases by 1	Quantity decreased by 1	✅ Pass
Purchase Out-of-Stock Sweet	POST /api/sweets/:id/purchase	Error / cannot purchase	Error / cannot purchase	✅ Pass
Restock Sweet (Admin)	POST /api/sweets/:id/restock	Quantity increases	Quantity increased	✅ Pass


##Frontend Tests (React SPA)
Test Case	Steps	Expected Result	Actual Result	Status
Register via UI	Fill registration form	User registered	User registered	✅ Pass
Login via UI	Fill login form	Redirected to dashboard	Redirected to dashboard	✅ Pass
View all sweets	Dashboard loads sweets	All sweets displayed	All sweets displayed	✅ Pass
Search sweets	Use search/filter inputs	Filtered sweets displayed	Filtered sweets displayed	✅ Pass
Purchase sweet	Click "Purchase" button	Quantity decreases	Quantity decreases	✅ Pass
Admin add/update/delete	Admin panel operations	Changes reflected	Changes reflected	✅ Pass
