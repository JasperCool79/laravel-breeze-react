# Laravel Breeze - React Edition

## Introduction

> Laravel Breeze React is the implementation for react from [breeze-next](https://github.com/laravel/breeze-next). 

Laravel Breeze React is an implementing of the [Laravel Breeze](https://laravel.com/docs/starter-kits) authentication template for [Create React App](https://create-react-app.dev). All of the authentication boilerplate is already written for you - powered by [Laravel Sanctum](https://laravel.com/docs/sanctum), allowing you to quickly begin pairing your beautiful React frontend with a powerful Laravel backend.

## Quick Start

### Installation

First, create a React App compatible Laravel backend by installing Laravel Breeze into a [fresh Laravel application](https://laravel.com/docs/installation) and installing Breeze's API scaffolding:

```bash
# Create the Laravel application...
composer create-project --prefer-dist laravel/laravel:^8.0 LaravelBreeze

cd LaravelBreeze

# Install Breeze and dependencies...
composer require laravel/breeze

php artisan breeze:install api
```

Next, ensure that your application's `APP_URL` and `FRONTEND_URL` environment variables are set to `http://localhost:8000` and `http://localhost:3000`, respectively.

After defining the appropriate environment variables, you may serve the Laravel application using the `serve` Artisan command:

```bash
# Serve the application...
php artisan serve
```

Next, clone this repository and install its dependencies with `yarn install` or `npm install`. Then, copy the `.env.example` file to `.env` and supply the URL of your backend:

```
REACT_APP_BACKEND_URL=http://localhost:8000
```
Finally, run the application via `yarn start`. The application will be available at `http://localhost:3000`:

```
npm start
```

> Note: Currently, we recommend using `localhost` during local development of your backend and frontend to avoid CORS "Same-Origin" issues.

### Authentication Hook

This Create React application contains a custom `useAuth` React hook, designed to abstract all authentication logic away from your pages. In addition, the hook can be used to access the currently authenticated user:

```js
const Dashboard = () => {
    const { logout, user } = useAuth({ middleware: 'auth' })

    return (
        <>
            <p>{user?.name}</p>

            <button onClick={logout}>Sign out</button>
        </>
    )
}

export default Dashboard
```

## Built with

- [React](https://reactjs.org)
- [Create React App v5](https://create-react-app.dev)
- [React Router v6](https://reactrouter.com): Routing for React
- [Tailwind](https://tailwindcss.com): for UI
- [SWR](https://swr.vercel.app/): React Hooks for Data Fetching
- [Axios](https://www.npmjs.com/package/axios): Promise based HTTP client for the browser and node.js
- [Headlessui/react](https://headlessui.dev): for UI Components
- [Vercel](http://vercel.com): for hosting

## Credits
-   [Nilanth](https://github.com/nilanth)
-   [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.

## Deploy
</a>
<img src="https://www.netlify.com/img/deploy/button.svg" height="37.5px" />
</a>

## Support

Laravel Breeze React needs a ⭐️ from you. Don't forget to leave a star ⭐️
