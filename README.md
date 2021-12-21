Thanks for taking the time to checkout a selection of my work with [Theorem LTS](https://github.com/theoremlegal)! Given that their repositories are private, I've copied a selection of tickets and a PR I wrote as I was preparing to end my contract.

When I began with Theorem, the platform had hard-coded checks for a single user account belonging to our CEO. This allowed him to log into the platform and create/edit products without being part of any vendor organization, and while it helped speed up the process of getting content into our marketplace, it caused bugs and ultimately wasn't the solution we hoped for long term. 

As my contract was coming to an end, I began addressing the issue below and taking notes on a solution that would maintain the features built on the `DO NOT DELETE organization`. By referring instead to a new USER_ROLE, we were able to take the abilities of our CEO's account and apply them to any account. (The result also lended itself to some pretty exciting debugging/developer tools)

![image](https://user-images.githubusercontent.com/62047446/146981531-a695ef0d-30fc-406c-ae6f-9dbad4096914.png)


