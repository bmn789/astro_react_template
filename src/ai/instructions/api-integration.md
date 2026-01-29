# API Integration Instructions

Follow these guidelines when creating new API services:

## File Naming
- Create service files in `src/services/`.
- Use the naming convention: `[feature].service.ts` (e.g., `profile.service.ts`, `auth.service.ts`).

## Code Structure

### 1. Imports
- Import `axios` for making HTTP requests.
- Define necessary TypeScript interfaces for request bodies and response data.

### 2. Service Object Naming
- Define the service object using a `const` variable.
- Use **UPPERCASE** for the service object name (e.g., `const PROFILE`, `const AUTH`).

### 3. Implementation
- implementation of the service object should be an object containing `async` methods.
- Each method should handle the API call and return `response.data`.
- Use proper typing for arguments and return values.

### 4. Export
- Export the service object as the **default** export.

## Example

```typescript
import axios from "axios"

export interface UserData {
    id: string
    name: string
    email: string
}

const USER = {
    async getById(id: string): Promise<UserData> {
        const response = await axios.get<UserData>(`/api/users/${id}`)
        return response.data
    },

    async update(id: string, body: Partial<UserData>): Promise<UserData> {
        const response = await axios.put<UserData>(`/api/users/${id}`, body)
        return response.data
    }
}

export default USER
```
