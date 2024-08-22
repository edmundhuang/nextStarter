### seed error
> The script uses bcrypt to hash the user's password, if bcrypt isn't compatible with your environment, you can update the script to use bcryptjs instead.

### Fix procedure
1. install bcryptjs
```
pnmp i bcryptjs
```
2. update route.ts as below
```
// import bcrypt from 'bcrypt';
var bcrypt= require('bcryptjs');
```

### Partial Prerendering (PPR).
1. next.config.mjs
```
/** @type {import('next').NextConfig} */
 
const nextConfig = {
  experimental: {
    ppr: 'incremental',
  },
};
 
export default nextConfig;
```

2.  layout.tsx
```
//...
 
export const experimental_ppr = true;
 
// ...
```

That is all.

