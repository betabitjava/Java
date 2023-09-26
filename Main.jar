import com.github.jmatss.bencode.BencodeOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.security.NoSuchAlgorithmException;
import java.util.HashMap;
import java.util.Map;

public class TorrentFileCreator {
    public static void main(String[] args) throws IOException, NoSuchAlgorithmException {
        // Путь к большому файлу, который вы хотите раздавать
        File fileToShare = new File("путь_к_вашему_большому_файлу");

        // Создание базовой информации для .torrent файла
        Map<String, Object> torrentInfo = new HashMap<>();
        torrentInfo.put("name", fileToShare.getName());
        torrentInfo.put("length", fileToShare.length());

        // Вычисление SHA-1 хеша файла (требуется для проверки целостности данных)
        // Здесь вам понадобится использовать библиотеку для вычисления хеша, например, java.security.MessageDigest.
        // Для примера, здесь используется заглушка.
        byte[] fileHash = new byte[]{0x01, 0x23, 0x45, 0x67};

        torrentInfo.put("sha1", fileHash);

        // Создание основного объекта .torrent
        Map<String, Object> torrentFile = new HashMap<>();
        torrentFile.put("announce", "http://your-tracker-url.com"); // URL трекера
        torrentFile.put("info", torrentInfo);

        // Сохранение .torrent файла на диск
        try (FileOutputStream fos = new FileOutputStream("ваш_файл.torrent")) {
            BencodeOutputStream out = new BencodeOutputStream(fos);
            out.writeObject(torrentFile);
            out.close();
        }
    }
}
        public class Main {
            public static void main(String[] args) {
                System.out.println("Hello world!");
            }
        }

