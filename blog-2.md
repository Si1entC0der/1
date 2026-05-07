# Mastering Utility Types: Pick and Omit for DRY Code

Efficiency in TypeScript isn't just about writing code that works; it’s about writing code that is maintainable. One of the best ways to keep your code **DRY (Don't Repeat Yourself)** is by using utility types like `Pick` and `Omit`.

### Avoiding Interface Bloat
Imagine you have a master `User` interface with dozens of fields. When creating a profile update page, you might only need a few of those fields. Instead of creating a brand-new interface, you can "slice" the existing one.

### Pick: Selecting What You Need
The `Pick` utility allows you to create a new type by choosing a specific set of keys from an existing interface.

```typescript
interface User {
  id: string;
  name: string;
  email: string;
  address: string;
  joinDate: Date;
}

type UserContactInfo = Pick<User, "name" | "email">;
```

### Omit: Removing the Sensitive Data
Conversely, `Omit` allows you to create a type by taking all properties from an interface except for a few specific ones. This is particularly useful for excluding sensitive fields like passwords or internal IDs.

```typescript
type UserPublicProfile = Omit<User, "id" | "address">;
```

### Conclusion
Using `Pick` and `Omit` ensures that if you ever update the master `User` interface (e.g., changing the `name` type), all your specialized slices update automatically. This single source of truth is the key to scalable TypeScript architecture.