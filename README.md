# WOT

1. run this code
    rails new ml6 --database=postgresql && cd ml6 && rails g scaffold Artist name:string && rails g scaffold Album title:string artist:belongs_to && rake db:create && rake db:migrate && rails s

2. display artist name on album list page
    album\index.html.erb
    <td><%= album.artist.name %></td>

3. change album form, adding artist select box
    album\_form.html.erb
    <%= form.collection_select :artist_id, Artist.all, :id, :name, include_blank: true %>

4. seed the database with a list of albums not associate to an artist_id
    http://www.xyzpub.com/en/ruby-on-rails/3.2/seed_rb.html

5. change the artist form, allowing users to select albums not associated with an artist
    http://www.xyzpub.com/en/ruby-on-rails/3.2/seed_rb.html
