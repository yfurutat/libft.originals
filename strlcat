//arg[2]==NULL -> segv!!!
//arg[2]!=NULL && arg[1]==NULL && arg[3] >0 ->segv!
//arg[2]!=NULL && arg[1]==NULL && arg[3]==0 
//->return: strlen(arg2) & dst = (null)!!!

int	main()
{
  char *dst1 = ft_calloc(100, sizeof(char));
	char *dst2 = ft_calloc(100, sizeof(char));
	printf("1. %zu %s\n", strlcat(dst1, "", 100), dst1);
	printf("2. %zu %s\n", strlcat(dst1, "hello ", 100), dst1);
	printf("3. %zu %s\n", strlcat(dst1, "world", 100), dst1);
	printf("4. %zu %s\n", strlcat(dst1, "world", SIZE_MAX), dst1);//16 hello worldworld
	printf("5. %zu %s\n", strlcat(dst1, "world", SIZE_MAX+1), dst1);//5 hello worldworld
	printf("6. %zu %s\n", strlcat(dst1, "world", SIZE_MAX-1), dst1);//21 hello worldworldworld
  free(dst1);
	free(dst2);
  dst1 = NULL;
  printf("   4. %lu %s\n", strlcat(dst1, NULL, 0), dst1);//segv
	printf("   4. %lu %s\n", strlcat(dst1, NULL, 2), dst1);//segv
	printf("   4. %lu %s\n", strlcat(dst1, NULL, 100000), dst1);//segv
	printf("   5. %lu %s\n", strlcat(dst1, "", 2), dst1);//segv
	printf("   6. %lu %s\n", strlcat(dst1, "", 0), dst1);//0 (null)
	printf("   7. %lu %s\n", strlcat(dst1, "is", 0), dst1);//2 (null)
	dst1 = "";
	printf("   8. %lu %s\n", strlcat(dst1, "", 0), dst1);//0
	// printf("   9. %lu %s\n", strlcat(dst1, NULL, 0), dst1);//segv
	// printf("   9. %lu %s\n", strlcat(dst1, NULL, 5), dst1);//segv
	dst1 = "hello world";
	// printf("   9. %lu %s\n", strlcat(dst1, NULL, 0), dst1);//segv
	// printf("   9. %lu %s\n", strlcat(dst1, NULL, 10), dst1);//segv
	printf("   9. %lu %s\n", strlcat(dst1, "", 0), dst1);//0 hello world
	printf("  10. %lu %s\n", strlcat(dst1, "abc", 0), dst1);//3 hello world
	printf("  11. %lu %s\n", strlcat(dst1, "!!!hello world!!!", 0), dst1);//17 hello world
  return (0);
}
