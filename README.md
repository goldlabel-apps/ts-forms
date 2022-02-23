# ts-forms

## [forked from react-hook-form](https://react-hook-form.com)

### Install
```bash
npm install -save @listingslab/ts-forms
```

### Quickstart
```jsx
import React from 'react';
import { useForm } from 'react-hook-form';
function App() {
  const { register, handleSubmit, errors } = useForm(); // initialize the hook
  const onSubmit = (data) => {
    console.log(data);
  };

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input name="firstname" ref={register} /> {/* register an input */}
      <input name="lastname" ref={register({ required: true })} />
      {errors.lastname && 'Last name is required.'}
      <input name="age" ref={register({ pattern: /\d+/ })} />
      {errors.age && 'Please enter number for age.'}
      <input type="submit" />
    </form>
  );
}
```

#### Key react-hook-form features

- Built with performance and DX in mind
- Embrace native form validation
- Simple integration with [UI libraries](https://codesandbox.io/s/react-hook-form-v6-controller-qsd8r)
- [Tiny size](https://bundlephobia.com/result?p=react-hook-form@latest) without any dependency
- Follows HTML standard for [validation](https://react-hook-form.com/get-started#Applyvalidation)
- [Resolvers](https://github.com/react-hook-form/resolvers) support [Yup](https://github.com/jquense/yup), [Zod](https://github.com/vriad/zod), [Superstruct](https://github.com/ianstormtaylor/superstruct), [Joi](https://github.com/hapijs/joi) or custom

#### react-hook-form docs

- [Motivation](https://medium.com/@bruce1049/form-validation-with-hook-in-3kb-c5414edf7d64)
- [Video tutorial](https://www.youtube.com/watch?v=-mFXqOaqgZk&t)
- [Get started](https://react-hook-form.com/get-started)
- [API](https://react-hook-form.com/api)
- [Examples](https://github.com/bluebill1049/react-hook-form/tree/master/examples)
- [Form Builder](https://react-hook-form.com/form-builder)
- [FAQs](https://react-hook-form.com/faqs)

#### Tags
react, hooks, npm, react-hook-form