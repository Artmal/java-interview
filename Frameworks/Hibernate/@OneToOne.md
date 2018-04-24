## `@OneToOne` mapping
The best way to map a `@OneToOne` relationship is to use `@MapsId`.

    @Entity(name = "PostDetails")
    @Table(name = "post_details")
    public static class PostDetails {

        @Id
        @GeneratedValue
        private Long id;

        @OneToOne
        @JoinColumn(name = "post_id", unique = true)
        private Post post;
    }
