# docker

        Authentication authentication = SecurityContextHolder.getContext().getAuthentication();
        String username = authentication.getName();
        String role = authentication.getAuthorities().stream().findFirst().get().getAuthority();

        // Atribui valores ao usuário logado
        http.userDetailsService(userDetailsService(username, role));
