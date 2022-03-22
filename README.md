<h1 align="center">Printf</h1>
<h4>For this project you will have to replicate the function printf. Once you pass the project you are allowed to use it in future projects!</h4>

## 📖 Content 📖

### 📚 Mandatory Part 📚

- **Name of the program** : `libftprintf.a`
- **Prototype** : `ft_printf(const char *, ...);`
- **Files** : [`*.c`](./src) [`ft_printf.h`](./include/ft_printf.h) [`Makefile`](./Makefile)
- **Makefile rules** : `all` `clean` `fclean` `re`
- **Authorized functions** : [`malloc`](https://man7.org/linux/man-pages/man3/free.3.html) [`free`](https://man7.org/linux/man-pages/man3/free.3.html) [`write`](https://man7.org/linux/man-pages/man2/write.2.html) [`va_start`](https://docs.microsoft.com/es-es/cpp/c-runtime-library/reference/va-arg-va-copy-va-end-va-start?view=msvc-170) [`va_arg`](https://docs.microsoft.com/es-es/cpp/c-runtime-library/reference/va-arg-va-copy-va-end-va-start?view=msvc-170) [`va_copy`](https://docs.microsoft.com/es-es/cpp/c-runtime-library/reference/va-arg-va-copy-va-end-va-start?view=msvc-170) [`va_end`](https://docs.microsoft.com/es-es/cpp/c-runtime-library/reference/va-arg-va-copy-va-end-va-start?view=msvc-170)
- [**Libft**](https://github.com/Zsolt42/Libft) **authorized**
- **Mandatory conversions** : `%c` (for printing characters) `%s` (for printing strings) `%p` (for printing a "void *" as hexadecimal) `%d` (for printing numbers in base 10) `%i` (for printing integers in base 10) `%u` (for printing unsigned integers in base 10) `%x & %X` (for printing hexadecimal numbers in base 16, lowercase and uppercase) `%%` (for printing %)

## 💣 Adding ft_Printf to your project 💣

#### To add ft_Printf in your project you should add this lines on your Makefile:

`LIBS_DIR	= libs`

`LIBS			= $(LIBS_DIR)/ft_printf/libftprintf.a \`

`LIBS_HEADERS	= -I $(LIBS_DIR)/ft_printf/include/ \`

#### Add in your `CFLAGS` rule:

`CFLAGS		= -Wall -Wextra -Werror -g $(LIB_HEADERS)`

#### Add in your `$(NAME): $(OBJ)`:

`$(NAME): $(OBJ) $(LIBS)`

`⠀⠀⠀⠀⠀⠀⠀⠀@$(CC) $(OBJ) $(LIBS) -o $(NAME)`

#### Add in your `%.o:%.c` rule:

`@$(CC) -c $(CFLAGS) -o $@ $^`

#### And last thing is to add a new rule:

`$(LIBS_DIR)/ft_printf/libftprintf.a:`

`⠀⠀⠀⠀⠀⠀⠀⠀@make -C $(LIBS_DIR)/ft_printf`

#### If you want to include your own libraries too:

`INC				= -I $("YOUR_INCLUDE_DIR") $(LIBS_HEADERS)`

`CFLAGS		= -Wall -Wextra -Werror -g $(INC)`

#### Anyway, I have some [`C templates`](https://github.com/Zsolt42/42_Cursus_zpalfi/tree/main/C_Templates) if you want to see more clearly how to do it 😄😄

## 💯 Mark 💯

<p align="center">
  <a align="center">
    <img src="./Addings/Mark.png">
  </a>
</p>
