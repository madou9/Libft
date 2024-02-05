The repository https://github.com/alelievr/libft-unit-test is a great resource for automatically testing and benchmarking your libft library. This tutorial should help you with installing and using these tests.

Before Installing The Tests
You should already have all the required files (ft_*.c, libft.h, Makefile) in your libft directory, even if your .c files or libft.h are empty.
Your Makefile to create libft.a should already be working. I am not allowed to share working code here but what your Makefile should do is:
Create .o files from your .c files
Create libft.a from those .o files.
A good resource to learn about Makefile is www.makefiletutorial.com and https://www.gnu.org/software/make/.

Installing The Tests
Rename your local libft directory/repo to "libft".
Change to the libft's parent directory and clone the libft-unit-test repository:
git clone https://github.com/alelievr/libft-unit-test.git
Your folder structure should now look like this:

.
|- libft/
|- libft-unit-tests/
Edit libft/Makefile and add the following rule to the bottom:
so:
	$(CC) -nostartfiles -fPIC $(CFLAGS) $(SRC)
	gcc -nostartfiles -shared -o libft.so $(OBJ)
Change $(CC), $(SRC) and $(OBJ) to the variable names you used for your compiler, your source and object files in your Makefile. You don't need to change $(CFLAGS) even if you haven't defined this variable.

Change to the libft-unit-tests directory
Complete the installation by running
make
Your tests should be correctly installed now!
