This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.



If the NextJS file opens in a localhost:3000 file, change the following lines in the following files:
- pages/[id]/edit.js in line 27 change const res = await fetch(`http://localhost:3001/api/notes/${router.query.id}`, {
  with const res = await fetch(`http://localhost:3000/api/notes/${router.query.id}`, { 
  and in line 163 change  const res = await fetch(`http://localhost:3001/api/notes/${id}`); to const res = await fetch(`http://localhost:3000/api/notes/${id}`);

- pages/[id]/index.js in line 25 change const deleted = await fetch(`http://localhost:3001/api/notes/${noteId}`, {
  with const deleted = await fetch(`http://localhost:3000/api/notes/${noteId}`, {
  and in line 61 change const res = await fetch(`http://localhost:3001/api/notes/${id}`); with   const res = await fetch(`http://localhost:3000/api/notes/${id}`);  
  
- pages/index.js in line 52 change const res = await fetch('http://localhost:3001/api/notes'); with   const res = await fetch('http://localhost:3000/api/notes');  
- pages/new.js in line 29 change const res = await fetch('http://localhost:3001/api/notes', { with const res = await fetch('http://localhost:3000/api/notes', {

Don't forget to save all files after changing the localhost port number if it opens at localhost:3000 on your local computer. 


  
You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
